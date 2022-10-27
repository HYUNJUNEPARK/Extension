# Extension

```kotlin
object Extension {
    fun Context.showToast(msg: String) = Toast.makeText(this, msg, Toast.LENGTH_SHORT).show()

    fun Long.convertLongToTime(): String {
      val date = Date(this)
      val format = SimpleDateFormat("HH:mm")
      return format.format(date)
    }

    fun ByteArray.toHex(): String = joinToString(separator = "") { eachByte -> 
        "%02x".format(eachByte) 
    }
}

```

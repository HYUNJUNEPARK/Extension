# Kotlin_Reference

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

```kotlin
enum class Color(val rgb: Int){
    RED(0xFF0000),
    GREEN(0x00FF00),
    BLUE(0x0000FF),
    YELLOW( 0xFFFF00);

    fun containsRed() = (this.rgb and 0xFF000 != 0)
}
```

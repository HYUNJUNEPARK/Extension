# Extension

```kotlin
fun Context.toast(msg: String) = Toast.makeText(this, msg, Toast.LENGTH_SHORT).show()

fun Long.convertLongToTime(): String {
  val date = Date(this)
  val format = SimpleDateFormat("HH:mm")
  return format.format(date)
}

```

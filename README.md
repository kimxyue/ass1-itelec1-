# ass1-itelec1-
override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
    setContentView(R.layout.activity_main)

    // Example: Initialize UI components
    val message = findViewById<TextView>(R.id.textView)
    message.text = "Hello, this screen was created!"
}

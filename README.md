# ass1-itelec1-
override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
    setContentView(R.layout.activity_main)

    // Example: Initialize UI components
    val message = findViewById<TextView>(R.id.textView)
    message.text = "Hello, this screen was created!"
}

override fun onStart() {
    super.onStart()

    // Example: Show a welcome message when screen is visible
    Toast.makeText(this, "Welcome! The Activity is visible.", Toast.LENGTH_SHORT).show()
}

override fun onResume() {
    super.onResume()

    // Example: Restart a counter or resume animations
    Log.d("LifecycleDemo", "[onResume] → Activity is interactive now")
}

override fun onPause() {
    super.onPause()

    // Example: Save temporary data before leaving screen
    val prefs = getSharedPreferences("MyPrefs", MODE_PRIVATE)
    prefs.edit().putString("draft", "User input text").apply()
}

override fun onStop() {
    super.onStop()

    // Example: Stop background work that isn’t needed
    Log.d("LifecycleDemo", "[onStop] → Activity is completely hidden now")
}

override fun onDestroy() {
    super.onDestroy()

    // Example: Clean up resources before Activity is removed
    Log.d("LifecycleDemo", "[onDestroy] → Cleaning up resources")
}

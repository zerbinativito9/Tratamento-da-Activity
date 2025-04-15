package com.example.activity

import android.os.Bundle
import android.widget.Toast
import androidx.activity.enableEdgeToEdge
import androidx.appcompat.app.AppCompatActivity
import androidx.core.view.ViewCompat
import androidx.core.view.WindowInsetsCompat

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        enableEdgeToEdge()
        setContentView(R.layout.activity_main)
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main)) { v, insets ->
            val systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars())
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom)
            insets
        }
    }
    override fun onStart(){
        super.onStart()
        Toast.makeText(applicationContext, "Método OnStart", Toast.LENGTH_SHORT).show();
    }
    override fun onRestart(){
        super.onRestart()
        Toast.makeText(applicationContext, "Método OnRestart", Toast.LENGTH_SHORT).show();
    }
    override fun onResume(){
        super.onResume()
        Toast.makeText(applicationContext, "Método OnResume", Toast.LENGTH_SHORT).show();
    }
    override fun onPause(){
        super.onPause()
        Toast.makeText(applicationContext, "Método OnPause", Toast.LENGTH_SHORT).show();
    }
    override fun onStop(){
        super.onStop()
        Toast.makeText(applicationContext, "Método OnStop", Toast.LENGTH_SHORT).show();
    }
    override fun onDestroy(){
        super.onDestroy()
        Toast.makeText(applicationContext, "Método OnDestroy", Toast.LENGTH_SHORT).show();
    }
}

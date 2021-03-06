# ShakeDetector
Better ShakeDetector Library that provides callback when shake started and ended along with onShakeCall.

Really easy to implement just setup the Detector onCreate

```
    @Override
    protected void onCreate(Bundle savedInstanceState) {
      super.onCreate(savedInstanceState);
      setContentView(R.layout.activity_demo);
      SensorManager sensorManager = (SensorManager) getSystemService(SENSOR_SERVICE);
      mShakeDetector = new ShakeDetector(sensorManager, this);
    }
    
    @Override
    public void onShakeStart() {
        Log.d(TAG, "Shaking Started");
    }

    @Override
    public void onShake() {
        Log.d(TAG, "Shaking");
    }

    @Override
    public void onShakeStop() {
        Log.d(TAG, "Shaking Ended");
    }

```

Check Sample App included that plays drum roll when device is shaken.

<img src="https://raw.githubusercontent.com/manijshrestha/ShakeDetector/master/sample_screen.png" width="300" />

Using the Library:
Add the following in your root level build.gradle
```
allprojects {
		repositories {
			...
			maven { url "https://jitpack.io" }
		}
	}
```

In your project build.gradle add the dependency
```
dependencies {
            ...
	        compile 'com.github.manijshrestha:ShakeDetector:1.0'
	}
```

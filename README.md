# Get-App-Version


### Step 1. Get App Version:
- Use the `PackageManager` to get information about your app, including the version name.
- You can obtain the version name using the following code snippet:
```bash
try {
    PackageInfo pInfo = getPackageManager().getPackageInfo(getPackageName(), 0);
    String version = pInfo.versionName;
    // Now, 'version' contains your app version name.
} catch (PackageManager.NameNotFoundException e) {
    e.printStackTrace();
}

```



### Step 2. Set App Version dynamically:
- In your activity or fragment code, after obtaining the app version, set it to the TextView.
```bash
TextView versionTextView = findViewById(R.id.versionTextView);
versionTextView.setText("Version: " + version);

```
Make sure to replace `version` with the actual version you obtained.

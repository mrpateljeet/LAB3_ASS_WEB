# Lab 3 Report

## Task 1 (Total 40 Points)

### A) Screenshots of Your App (5 Points)

### B) Differences Between Running the App on an Emulator versus a Physical Device

When running the app on an emulator and a physical device, you may notice the following differences:

- **Performance:** The physical device often runs the app more smoothly, with faster load times and fewer lags, especially with animations. Emulators may be slower, particularly on machines with limited resources.
- **User Interaction:** The physical device allows real touch gestures, like swipes and pinches, whereas the emulator mimics touch with mouse clicks, which isn’t as precise.
- **Hardware-Specific Features:** Certain features, like the camera or sensors, may not work as expected on an emulator but function correctly on a physical device.
- **Screen Resolution and Display:** Physical devices show the actual display quality, including color and brightness. Emulators approximate this, but physical devices may reveal UI issues related to screen size and aspect ratio more accurately.

---

## Setting Up an Emulator (10 Points)

### A) Steps to Set Up an Emulator in Android Studio or Xcode

1. **Install Xcode:** Download Xcode from the Mac App Store and open it once installed, following any initial setup instructions.
2. **Set Command Line Tools:** Go to Xcode > Preferences > Locations tab and select the version of Xcode you installed under Command Line Tools.
3. **Open the Simulator:** Open the Simulator from Xcode by navigating to Xcode > Open Developer Tool > Simulator.
4. **Set Up a New iOS Simulated Device:** Go to Window > Devices and Simulators, click the Simulators tab, press the + button to add a new simulator, and click Create.
5. **Start the Simulator:** Select the newly created simulator in the Devices and Simulators window and click Start to launch it.

### B) Challenges Faced and Solutions

- **SDK Version Compatibility:** Selecting a stable or recommended SDK version resolved compatibility issues.
- **Slow Performance:** Increasing RAM allocation for the emulator in AVD settings improved performance.
- **Device-Specific Issues:** Switching to another device model or Android version resolved unique bugs or crashes.

---

## Running the App on a Physical Device Using Expo (10 Points)

### A) Connecting the Physical Device

Installed the Expo CLI using the command `npm install -g expo-cli`. Expo Developer Tools opened in the browser, displaying a QR code. Installed the Expo Go App from the Apple Store, scanned the QR code with the device, and loaded the app.

### B) Troubleshooting Steps

- **Network Issues:** Ensured both computer and mobile device were connected to the same Wi-Fi network.
- **App Not Loading:** Restarted the Expo server and cleared the cache using `expo start -c`.

---

## Comparison of Emulator vs. Physical Device (10 Points)

| **Aspect**          | **Emulator**                            | **Physical Device**                        |
|---------------------|-----------------------------------------|-------------------------------------------|
| **Performance**     | Slower on lower-end machines            | Faster, showing real-world app performance|
| **Touch Accuracy**  | Simulated with mouse clicks             | Natural touch gestures                    |
| **Hardware Access** | Limited access (e.g., camera, GPS)      | Full access to all hardware features      |
| **Screen Quality**  | Approximate colors and resolution       | True screen quality and color display     |
| **Testing Scope**   | Easy to test on multiple devices        | Limited to a specific device              |

**Advantages and Disadvantages:**

- **Advantages of Emulator:** Quick testing on various versions and screen sizes; simulated environment without physical devices.
- **Advantages of Physical Device:** Accurate representation of real-world usage; access to hardware-dependent features.
- **Disadvantages of Emulator:** Slower performance, limited hardware access, inaccurate display.
- **Disadvantages of Physical Device:** Limited to single device testing, network dependency.

---

## Troubleshooting a Common Error (5 Points)

A common error encountered: *“Unable to load script”* due to Metro Bundler connection issues. Resolved by ensuring the device and computer are on the same network and clearing cache.

---

## Task 2: Building a Simple To-Do List App (60 Points)

### Explanation of Features Implemented

- **Add New Tasks:** The `handleTaskSubmit` function adds new tasks if the input is not empty.
- **Update Existing Tasks:** Users can edit tasks, changing the input field and button state.
- **Delete Tasks:** Tasks can be deleted with a confirmation alert.
- **Scrollable Task List:** Implemented with `FlatList` for scrollability.
- **User-Friendly Interface:** Clear buttons, animations for task management.

### Explanation of Code

- **State Management:** `useState` and `useEffect` manage state and persist tasks.
- **Adding a Task:** `addTask` function creates new tasks with unique IDs.
- **Deleting a Task:** `deleteTask` function removes tasks from the state.
- **Toggling Completion:** `toggleTaskCompletion` applies strikethrough styles to completed tasks.
- **Rendering the List:** Used `FlatList` to display tasks with deletion and completion toggling capabilities.

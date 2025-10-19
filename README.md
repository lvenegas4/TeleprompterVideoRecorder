# Recording Teleprompter

A browser-based teleprompter application that allows you to record video presentations while reading from a scrolling script. The application uses browser APIs to access your camera and microphone, display a scrolling teleprompter, and save your recordings locally.

## Features

- **Camera and Microphone Access**: Select from available video and audio input devices
- **Scrolling Teleprompter**: Adjustable scroll speed and font size for comfortable reading
- **Video Recording**: Records video with audio while displaying the teleprompter
- **Background Effects**: Apply real-time filters including blur, brightness, contrast, and saturation
- **Mirrored Camera Feed**: See yourself as you would in a mirror while recording
- **Local Recording**: All recordings are saved locally to your device
- **Automatic Stop**: Recording stops automatically when the script ends

## Requirements

- Modern web browser with support for:
  - MediaDevices API (camera/microphone access)
  - MediaRecorder API (video recording)
  - getUserMedia API
- Camera and microphone permissions

## Usage

1. Open `teleprompter.html` in a web browser
2. Grant camera and microphone permissions when prompted
3. Select your preferred camera and microphone from the dropdown menus
4. Paste or type your script in the text area
5. Adjust settings as needed:
   - **Scroll Speed**: Control how fast the text scrolls (1-100)
   - **Font Size**: Set text size for comfortable reading (12-120px)
   - **Blur**: Apply background blur effect (0-20px)
   - **Brightness**: Adjust video brightness (50-150%)
   - **Contrast**: Modify video contrast (50-150%)
   - **Saturation**: Control color intensity (0-200%)
6. Click "Start Prompter & Record" to begin
7. Read from the teleprompter while recording
8. Click "Stop" or press the Escape key to end the recording
9. Download your video using the provided download link

## Technical Details

- **Video Format**: WebM with VP9 codec
- **Recording Mode**: Continuous recording with 10ms data chunks
- **File Naming**: Automatic timestamp-based naming (teleprompter-recording-YYYY-MM-DDTHH-MM-SS.webm)
- **Camera Display**: Horizontally flipped for natural viewing experience
- **Teleprompter Position**: Top quarter of the screen with semi-transparent background

## Keyboard Shortcuts

- **Escape**: Stop recording and close teleprompter

## Browser Compatibility

Tested and working in:
- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Safari (with appropriate permissions)

## Privacy

All recording and processing happens entirely in your browser. No data is sent to external servers. Recordings are saved directly to your local device.

## File Structure

```
TELEPROMPTER/
└── teleprompter.html    # Main application file (HTML, CSS, and JavaScript)
```

## Customization

You can modify the following in the HTML file:
- Color scheme (Tailwind CSS classes)
- Default settings values
- Teleprompter window size and position
- Font family (currently using Inter font from Google Fonts)
- Filter ranges and step values

## Troubleshooting

**Camera/Microphone not working**
- Ensure you've granted browser permissions for camera and microphone access
- Check that your devices are properly connected and not in use by another application
- Try refreshing the page and granting permissions again

**Recording not starting**
- Make sure you've entered text in the script area
- Verify that both camera and microphone are selected and active
- Check browser console for error messages

**Download not working**
- Ensure the recording was stopped properly
- Try a different browser if downloads aren't initiating
- Check your browser's download settings and permissions

## License

This project is provided as-is for personal and commercial use.

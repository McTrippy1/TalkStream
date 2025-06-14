# TalkStream

TalkStream is a real-time chatroom application built with Windows Forms and C#. It utilizes HTTP polling (with optional WebSocket integration planned) to communicate with a PHP-based backend for message persistence. The application features real-time notifications, a dynamic window title that includes the machine name, and the ability to embed external files (like a notification sound) into a single executable.

## Features

- **Real-Time Chat:** Send and receive messages in near real-time.
- **Typing Indicator:** See who is typing in the chatroom.
- **Notification Sound:** Plays an embedded notification sound when a new message arrives (only fires when the application is minimized and conditions are met).
- **Dynamic Title:** The window title updates to show `TalkStream - [COMPUTERNAME]`.
- **Cross-Platform Extension:** Future plans include mobile ports and WebSocket support for improved performance and responsiveness.

## Prerequisites

- **.NET Framework 4.7.2** (or later) installed on your system  
- **Visual Studio** for development and debugging  
- A **PHP/MySQL backend** deployed to manage the messages and typing indicators.

## Usage

1. **Run the Application:**

    Start the built executable. The window title will display as `TalkStream - [YourMachineName]`.

2. **Chat Functionality:**

    - Type your message in the input field and press Enter to send.
    - Incoming messages from other users will be shown in the conversation pane.
    - When the application is minimized, a notification sound will play if a message is received (after 5 seconds from startup).

3. **Backend API Endpoints:**

    The application interacts with the following backend endpoints:
    - `getMessages.php?lastId=...` for retrieving new messages.
    - `postMessage.php` to send a message.
    - `getTyping.php` for updating typing indicators.
    - `updateTyping.php` to notify the backend when the user is typing.

## Future Improvements

- **WebSocket Integration:**  
  Implement a WebSocket server to replace the HTTP polling for improved performance.
  
- **Mobile Port:**  
  Explore options to port TalkStream to mobile platforms (e.g., using Xamarin.Forms or .NET MAUI) while leveraging the same backend.

- **UI Enhancements:**  
  Improve user interface responsiveness and styling based on user feedback.

## License

This project is licensed under the [MIT License](LICENSE).

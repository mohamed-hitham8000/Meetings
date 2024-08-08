# Meetings
Meetings video call and chat















<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meetings</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        #meeting-container {
            width: 80%;
            margin: 40px auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        #video-container {
            width: 100%;
            height: 800px;
            border: 1px solid #ccc;
            border-radius: 10px;
            overflow: hidden;
        }
        #video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        #chat-container {
            width: 100%;
            height: 200px;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 10px;
            overflow-y: auto;
        }
        #chat-log {
            padding: 10px;
        }
        #message-input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 10px;
        }
        #send-button {
            width: 100%;
            padding: 10px;
            background-color: #4CAF50;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        #record-button {
            width: 100%;
            padding: 10px;
            background-color: #FF69B4;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        #invite-button {
            width: 100%;
            padding: 10px;
            background-color: #337AB7;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        #invite-code-input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <div id="meeting-container">
        <h2>Meetings</h2>
        <div id="video-container">
            <video id="video" autoplay playsinline></video>
        </div>
        <div id="chat-container">
            <div id="chat-log"></div>
            <input id="message-input" type="text" placeholder="Type a message...">
            <button id="send-button">Send</button>
            <button id="record-button">Record Screen</button>
            <button id="invite-button">Invite People</button>
            <input id="invite-code-input" type="text" placeholder="Enter invite code...">
            <button id="join-button">Join Meeting</button>
        </div>
    </div>

    <script src="js.js"></script>
</body>
</html>







const video = document.getElementById('video');
const chatLog = document.getElementById('chat-log');
const messageInput = document.getElementById('message-input');
const sendButton = document.getElementById('send-button');
const recordButton = document.getElementById('record-button');
const inviteButton = document.getElementById('invite-button');
const inviteCodeInput = document.getElementById('invite-code-input');
const joinButton = document.getElementById('join-button');

let meetingCode = '';
let stream = null;

// Request access to camera and microphone
navigator.mediaDevices.getUserMedia({ video: true, audio: true })
    .then(stream => {
        video.srcObject = stream;
        this.stream = stream;
    })
    .catch(error => {
        console.error('Error getting user media:', error);
    });

// Generate a unique meeting code when the "Invite People" button is clicked
inviteButton.addEventListener('click', () => {
    meetingCode = generateMeetingCode();
    alert(`Meeting code: ${meetingCode}`);
});

// Generate a random meeting code
function generateMeetingCode() {
    return Math.random().toString(36).substr(2, 6);
}

// Handle joining a meeting when the "Join Meeting" button is clicked
joinButton.addEventListener('click', () => {
    const enteredCode = inviteCodeInput.value.trim();
    if (enteredCode === meetingCode) {
        // Join the meeting logic here
        alert('You have joined the meeting!');
    } else {
        alert('Invalid meeting code');
    }
});







































:root {
  --primary-color: blue;
  --accent-color: orange;
}

h1 {
  color: var(--primary-color);
}

button {
  background-color: var(--accent-color);
}























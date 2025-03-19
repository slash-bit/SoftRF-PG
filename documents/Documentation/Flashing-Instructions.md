<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SenseCap T1000E Firmware Flashing Instructions</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            background-color: #f9f9f9;
        }

        h1 {
            color: #333;
        }

        ul {
            margin: 20px 0;
            padding: 0;
            list-style: none;
        }

        ul li {
            margin-bottom: 10px;
        }

        ul li ul {
            margin-left: 20px;
            list-style: circle;
        }

        img {
            max-width: 100%;
            height: auto;
            margin: 20px 0;
            display: block;
        }

        .instruction-step {
            margin-bottom: 15px;
            padding: 10px;
            background-color: #fff;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <h1>SenseCap T1000E Firmware Flashing Instructions</h1>
    <p>To flash the T1000E, follow these steps:</p>
    <ul>
        <li class="instruction-step">First, power on the T1000E.</li>
        <li class="instruction-step">Connect the T1000E to your PC using a USB cable.</li>
        <li class="instruction-step">Put the device into <strong>DFU mode</strong>:
            <ul>
                <li>Press and hold the device button.</li>
                <li>Quickly connect the charging cable <strong>twice</strong> (double flick).</li>
                <li>The green LED will turn solid. See the animation below for guidance:</li>
            </ul>
            <img src="https://github.com/user-attachments/assets/78301873-671b-444d-8780-5e28b84568eb" alt="T1000E Double Flick GIF">
        </li>
        <li class="instruction-step">Once the device is in DFU mode, a disk drive named <strong>"T1000-E"</strong> will appear on your PC.</li>
        <li class="instruction-step">Drag and drop the downloaded firmware file into this drive:
            <img src="https://github.com/user-attachments/assets/99fa836a-365b-4166-87b2-2905cc2ebe9b" alt="Firmware Drag and Drop" style="width: 290px;">
        </li>
        <li class="instruction-step">Once the file is copied, the window will automatically close.</li>
        <li class="instruction-step">The T1000E will update and shut down.</li>
        <li class="instruction-step">Power on the device by pressing the button once.</li>
    </ul>
</body>
</html>

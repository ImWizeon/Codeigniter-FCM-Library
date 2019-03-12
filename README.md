# Codeigniter-FCM-Library

A simple codeigniter library for Firebase Cloud messaging.\
This is a very simple implementation of firebase cloud messaging library for codeigniter 3.*

## Installation

Put the config file in the **application/config** folder.\
Similarly copy the [Fcm.php](https://github.com/owizeo/Codeigniter-FCM-Library/blob/master/library/Fcm.php) file to the codeigniters **application/libraries** folder.



## Usage


```
public function sendNotification()
{
   $token = 'Registratin_id'; // push token
   $message = "Test notification message";
   $this->load->library('fcm');
   $this->fcm->setTitle('Test FCM Notification');
   $this->fcm->setMessage($message);
   $json = $this->fcm->getPush();
   $p = $this->fcm->send($token, $json);
}
````
Examples are in the [example_controller.php](https://github.com/owizeo/Codeigniter-FCM-Library/blob/master/example_controller.php) file.

## License
[MIT](https://github.com/owizeo/Codeigniter-FCM-Library/blob/master/LICENSE)

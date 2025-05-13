# WiFi Direct Legacy - Status doesn't update
A reproduction showing that the c# `WiFiDirectAdvertisementPublisher` class doesn't update its status after it's network is Started.

What works: the WiFi Direct Legacy network will not start and  and `Publisher.Status` will be `Aborted` when running the sample code with WiFi switched off through the Modern UI Settings (e.g. via the taskbar or via  `ms-settings:network-wifi`).

What doesn't work: when the sample code is run with WiFi swiched on the network starts as expected, but switching the WiFi off while it's running will seemingly shut down the network and disconnect any connected devices without changing the `Publisher.Status` or invoking `Publisher.StatusChanged`.

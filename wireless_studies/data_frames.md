# Wireless data frames

802.11 specify frame types for use in transmission and management of wirless links

Frames are divided into specific and standardized sections.

Each frame consists of a MAC header, payload, and frame check sequence(FCS).

The first two bytes of the MAC header form a frame control field specifying the form and function of the frame. This frame control field is subdivided into the following sub-fields:

* Protocol Version: Two bits representing the protocol version. Currently used protocol version is zero. Other values are reserved for future use.

* Type: Two bits identifying the type of WLAN frame. Control, Data, and Management are various frame types defined in IEEE 802.11.

* Subtype: Four bits providing additional discrimination between frames. Type and Sub Type together to identify the exact frame.

* ToDS and FromDS: Each is one bit in size. They indicate whether a data frame is headed for a distribution system. Control and management frames set these values to zero. All the data frames will have one of these bits set. However communication within an Independent Basic Service Set (IBSS) network always set these bits to zero.

* More Fragments: The More Fragments bit is set when a packet is divided into multiple frames for transmission. Every frame except the last frame of a packet will have this bit set.

* Retry: Sometimes frames require retransmission, and for this there is a Retry bit that is set to one when a frame is resent. This aids in the elimination of duplicate frames.

* Power Management: This bit indicates the power management state of the sender after the completion of a frame exchange. Access points are required to manage the connection, and will never set the power-saver bit.

* More Data: The More Data bit is used to buffer frames received in a distributed system. The access point uses this bit to facilitate stations in power-saver mode. It indicates that at least one frame is available, and addresses all stations connected.

* Protected Frame: The Protected Frame bit is set to one if the frame body is encrypted by a protection mechanism such as Wired Equivalent Privacy (WEP), Wi-Fi Protected Access (WPA), or Wi-FI Protected Access II (WPA2).

* Order: This bit is set only when the "strict ordering" delivery method is employed. Frames and fragments are not always sent in order as it causes a transmission performance penalty.


Next 2 bytes are reserved for Duration ID field. This field can take 3 forms: Duration, Contention-Free Period(Cfp) and Association ID (AID)

# Management Frames

Allow for the maintenance of communication.

TODO

# Control Frames

TODO

# Data Frames

TODO

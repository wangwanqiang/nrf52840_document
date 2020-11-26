# nrf52840_document

资源主页：https://www.nordicsemi.com/Software-and-tools/Development-Kits/nRF52840-DK/GetStarted#infotabs


## using as sniffer 

https://www.cnblogs.com/unrulife/p/10818248.html

Sniffer 官方软件下载
https://www.nordicsemi.com/Software-and-tools/Development-Tools/nRF-Sniffer-for-Bluetooth-LE/Download#infotabs



###  抓包的两种模式

The Sniffer has two modes of operation:
1.
Listens on all advertising channels to try to pick up as many packets as possible from as many
devices as possible.
2.
Follows one particular device and tries to catch all packets sent to or from this particular device.
This mode will catch all Advertisements and Scan Responses sent from the device, Scan Requests
and Connect Requests sent to the device, and all packets in the Connection sent between the two
devices in the Connection.
The Sniffer always starts in the first mode, showing information for all devices it receives packets from in the
Device List, as shown in Figure 3 on page 6. From this list, you can choose one particular device to sniff, and
by that change the mode of the sniffer. As shown in Table 1 on page 7, this is done by using either the arrow
keys and pressing enter or pressing a number from 0-9. You can at any time return to mode 1 by pressing l



### 蓝牙的各种查询



1：蓝牙广播类型查询

https://www.bluetooth.com/specifications/assigned-numbers/generic-access-profile/

2：SIG给各大公司分配的ID查询

https://www.bluetooth.com/specifications/assigned-numbers/company-identifiers/

3：蓝牙各种服务UUID查询

https://www.bluetooth.com/specifications/assigned-numbers/service-discovery/

4：蓝牙核心规范下载（最新规范5.2）

https://www.bluetooth.com/specifications/bluetooth-core-specification/

5：蓝牙Mesh规范下载

https://www.bluetooth.com/specifications/mesh-specifications/

6：传统蓝牙规范下载

https://www.bluetooth.com/specifications/profiles-overview/

7：蓝牙LE Audio LC3编码规范下载

https://www.bluetooth.com/specifications/le-audio/



### 抓到的苹果的数据的示例

```wireshark
Frame 88868: 63 bytes on wire (504 bits), 63 bytes captured (504 bits) on interface wireshark_extcap2304, id 0
Nordic BLE Sniffer
    Board: 6
    Header Version: 2, Packet counter: 57691
        Length of payload: 56
        Protocol version: 2
        Packet counter: 57691
        Packet ID: 6
    Length of packet: 10
    Flags: 0x01
        .... ...1 = CRC: OK
        .... ..0. = Reserved: 0
        .... .0.. = Reserved: 0
        .... 0... = Reserved: 0
        .000 .... = PHY: LE 1M (0)
        0... .... = Reserved: 0
    Channel: 39
    RSSI: -46 dBm
    Event counter: 0
    Delta time (end to start): 367µs
    [Delta time (start to start): 743µs]
    [Packet time (start to end): 376µs]
Bluetooth Low Energy Link Layer
    Access Address: 0x8e89bed6
    Packet Header: 0x2540 (PDU Type: ADV_IND, ChSel: #1, TxAdd: Random)
        .... 0000 = PDU Type: 0x0 ADV_IND
        ...0 .... = Reserved: 0
        ..0. .... = Channel Selection Algorithm: #1
        .1.. .... = Tx Address: Random
        0... .... = Reserved: 0
        Length: 37
    Advertising Address: 77:ca:64:2f:7e:2a (77:ca:64:2f:7e:2a)
    Advertising Data
        Flags
            Length: 2
            Type: Flags (0x01)
            000. .... = Reserved: 0x0
            ...1 .... = Simultaneous LE and BR/EDR to Same Device Capable (Host): true (0x1)
            .... 1... = Simultaneous LE and BR/EDR to Same Device Capable (Controller): true (0x1)
            .... .0.. = BR/EDR Not Supported: false (0x0)
            .... ..1. = LE General Discoverable Mode: true (0x1)
            .... ...0 = LE Limited Discoverable Mode: false (0x0)
        16-bit Service Class UUIDs
            Length: 27
            Type: 16-bit Service Class UUIDs (0x03)
            UUID 16: Unknown (0xb2dd)
            UUID 16: Unknown (0x6cda)
            UUID 16: Unknown (0x019f)
            UUID 16: Unknown (0x347a)
            UUID 16: Unknown (0x3db3)
            UUID 16: Unknown (0x381d)
            UUID 16: Unknown (0x4398)
            UUID 16: Unknown (0x806f)
            UUID 16: Unknown (0x0309)
            UUID 16: Unknown (0x6671)
            UUID 16: Unknown (0x9074)
            UUID 16: Unknown (0x4128)
            UUID 16: Unknown (0x378b)
    CRC: 0x62d1d2


```







# Tugas Hands On TCP dan UDP Jarkom

![Lambang ITS](https://www.its.ac.id/wp-content/uploads/2020/07/Lambang-ITS-2-320x320.png)

- Ligar Arsa Arnata (5025211244)

## Daftar isi

- [Tugas Hands On TCP dan UDP Jarkom](#tugas-hands-on-tcp-dan-udp-jarkom)
  - [Daftar Isi](#daftar-isi)
  - [Informasi](#informasi)
  - [TCP](#tcp)
    - [Soal Nomor 1](#soal-nomor-1-tcp)
    - [Jawaban Nomor 1](#jawaban-nomor-1-tcp)
      - [Filtering](#filtering-1-tcp)
      - [IP Address dan Port Number](#ip-address-dan-port-number-1)
    - [Soal Nomor 2](#soal-nomor-2-tcp)
    - [Jawaban Nomor 2](#jawaban-nomor-2-tcp)
      - [Filtering](#filtering-2-tcp)
      - [IP Address dan Port Number](#ip-address-dan-port-number-2)
    - [Soal Nomor 3](#soal-nomor-3-tcp)
    - [Jawaban Nomor 3](#jawaban-nomor-3-tcp)
      - [Filtering](#filtering-3-tcp)
      - [RAW Sequence Number](#raw-sequence-number-3)
    - [Soal Nomor 4](#soal-nomor-4-tcp)
    - [Jawaban Nomor 4](#jawaban-nomor-4-tcp)
      - [Filtering](#filtering-4-tcp)
      - [RAW Sequence Number](#raw-sequence-number-4)
      - [SYNACK Segment](#synack-segment-4)
      - [Acknowledgement Field](#acknowledgement-field-4)
      - [Explanation](#explanation-4-tcp)
    - [Soal Nomor 5](#soal-nomor-5-tcp)
    - [Jawaban Nomor 5](#jawaban-nomor-5-tcp)
      - [Filtering](#filtering-5-tcp)
      - [Sequence Number](#sequence-number-5)
    - [Soal Nomor 6](#soal-nomor-6-tcp)
    - [Jawaban Nomor 6](#jawaban-nomor-6-tcp)
      - [Filtering](#filtering-6-tcp)
      - [Arrival Time](#arrivel-time-6)
      - [Receiving Time](#receiving-time-6)
      - [RTT First Segment](#rtt-first-segment-6)
    - [Soal Nomor 7](#soal-nomor-7-tcp)
    - [Jawaban Nomor 7](#jawaban-nomor-7-tcp)
      - [Filtering](#filtering-7-tcp)
      - [First Frame Length](#first-frame-length-7)
      - [Second Frame Length](#second-frame-length-7)
  - [UDP](#udp)
    - [Soal Nomor 1](#soal-nomor-1-udp)
    - [Jawaban Nomor 1](#jawaban-nomor-1-udp)
      - [Filtering](#filtering-1-udp)
      - [Packet Number](#packet-number-1)
      - [Application Layer Payload](#application-layer-payload-1)
      - [UDP Header](#udp-header-1)
    - [Soal Nomor 2](#soal-nomor-2-udp)
      - [Explanation](#explanation-2-udp)
    - [Soal Nomor 3](#soal-nomor-3-udp)
      - [Explanation](#explanation-3-udp)
    - [Soal Nomor 4](#soal-nomor-4-udp)
      - [Explanation](#explanation-4-udp)
    - [Soal Nomor 5](#soal-nomor-5-udp)
      - [Explanation](#explanation-5-udp)
    - [Soal Nomor 6](#soal-nomor-6-udp)
      - [Explanation](#explanation-6-udp)
    - [Soal Nomor 7](#soal-nomor-7-udp)
      - [Jawaban Nomor 7](#jawaban-nomor-7-udp)
      - [First Packet Number](#first-packet-number-7)
      - [Second Packet Number](#second-packet-number-7)
      - [Explanation](#explanation-7-udp)



  ## Informasi

  Dalam melakukan hands on ini, saya melakukan capturing wireshark pada internet local saya dan melakukan step sesuai dengan PDF. Sehingga jawaban mungkin saja berbeda dengan file yang disediakan pada PDF.

  ## TCP

  ### Soal Nomor 1 TCP

  What is the IP address and TCP port number used by the client computer (source) that is transferring the alice.txt file to gaia.cs.umass.edu?

  ### Jawaban Nomor 1 TCP

  #### Filtering 1 TCP

  Masukkan filter `http.request.method == "POST"` pada display filter. Filter tersebut hanya akan menampilkan packet dengan protocol HTTP dan memiliki metode POST

  ![No1](https://cdn.discordapp.com/attachments/773324309020147732/1162593169809092648/image.png?ex=653c8043&is=652a0b43&hm=b763b2b83b8b99cd71f1035d2a65582b55b5c5c2a7b2a1bcd8e59df80da103f1&)

  #### IP Address dan Port Number 1

  Dari gambar diatas bisa dilihat bahwa IP Address dari client adalah **192.168.0.108** dan Port Numbernya **60182**
  


  ### Soal Nomor 2 TCP

  What is the IP address of gaia.cs.umass.edu ? On what port number is it sending and receiving TCP segments for this connection ?
  
  ### Jawaban Nomor 2 TCP

  #### Filtering 2 TCP

  Masukkan filter yang sama dengan nomor 1 `http.request.method == "POST"` pada display filter. Filter tersebut hanya akan menampilkan packet dengan protocol HTTP dan memiliki metode POST

  ![No2](https://cdn.discordapp.com/attachments/773324309020147732/1162593169809092648/image.png?ex=653c8043&is=652a0b43&hm=b763b2b83b8b99cd71f1035d2a65582b55b5c5c2a7b2a1bcd8e59df80da103f1&)

  #### IP Address dan Port Number 2

  Dari gambar diatas bisa dilihat bahwa IP Address dari gaia.cs.umass.edu  adalah **128.119.245.12** dan Port Numbernya **80**

  ### Soal Nomor 3 TCP

  What is the sequence number of the TCP SYN segment that is used to initiate the TCP connection between the client computer and gaia.cs.umass.edu ?

  ### Jawaban Nomor 3 TCP

  #### Filtering 3 TCP

  Masukkan filter `tcp.flags.syn == 1 and ip.dst == 128.119.245.12` pada display filter. Filter tersebut hanya akan menampilkan packet yang memiliki flag TCP SYN dengan tujuan ke gaia.cs.umass.edu

  #### RAW Sequence Number 3

  ![No3](https://cdn.discordapp.com/attachments/773324309020147732/1162594969622683688/image.png?ex=653c81f0&is=652a0cf0&hm=bcf41a0bf99bcb5795341fbdd46ed2274c8630058e8e9ed215b7c97bcd95c149&)

  Dari detail packet diatas yang didapatkan setelah dilakukan filtering, RAW Sequence Numbernya adalah **3332581985**


  ### Soal Nomor 4 TCP

  - What is the sequence number of the SYNACK segment sent by gaia.cs.umass.edu to the client computer in reply to the SYN ?
  - What is it in the segment that identifies the segment as a SYNACK segment ?
  - What is the value of the Acknowledgement field in the SYNACK segment ?
  - How did gaia.cs.umass.edu determine that value ?

  ### Jawaban Nomor 4 TCP

  #### Filtering 4 TCP

  Masukkan filter `tcp.flags.syn == 1 and tcp.flags.ack == 1 and ip.src == 128.119.245.12` pada display filter. Filter tersebut hanya akan menampilkan packet yang merupakan respon SYN/ACK dari gaia.cs.umass.edu ke client

  #### Raw Sequence Number 4

  ![No4](https://cdn.discordapp.com/attachments/773324309020147732/1162596212243955845/image.png?ex=653c8318&is=652a0e18&hm=7b3f5eb374806899e3b56c5131a574e47fbda41581d6f7e904e408dd633d75e5&)

   Dari detail packet diatas yang didapatkan setelah dilakukan filtering, RAW Sequence Numbernya adalah **4188397720**

  #### SYNACK Segment 4

  ![No4-1](https://cdn.discordapp.com/attachments/773324309020147732/1162597023527223386/image.png?ex=653c83da&is=652a0eda&hm=65cfb068c4254b2dc2fdaee116c7de6096e6f87b5a9346205675b1fd7f04c7b2&)

  Dari detail packet diatas yang didapatkan setelah dilakukan filtering yang sama, ditemukan bahwa segmen tersebut adalah SYN/ACK segment yang digunakan dalam proses inisiasi koneksi TCP karena kedua flag tersebut diatur (bernilai 1)

 #### Acknowledgement Field 4

 Dari 2 foto diatas, dapat ditemukan bahwa Acknowledge Field dari packet tersebut adalah **1**

 #### Explanation 4 TCP

 gaia.cs.umass.edu menentukan nilai Acknowledgment field dalam SYN/ACK segment dengan menambahkan 1 pada nomor urutan yang diterima dari paket SYN. Hal ini merupakan konvensi dalam protokol TCP bahwa Acknowledgment number dalam paket SYN/ACK adalah nomor urutan yang diterima sebelumnya (dalam paket SYN) ditambah 1.
  


  ### Soal Nomor 5 TCP

  What is the sequence number of the TCP segment containing the header of the HTTP POST command ?
  
  ### Jawaban Nomor 5 TCP

  #### Filtering 5 TCP

  Masukkan filter yang sama dengan nomor 1 `http.request.method == "POST"` pada display filter. Filter tersebut hanya akan menampilkan packet dengan protocol HTTP dan memiliki metode POST

  ![No5](https://cdn.discordapp.com/attachments/773324309020147732/1162593169809092648/image.png?ex=653c8043&is=652a0b43&hm=b763b2b83b8b99cd71f1035d2a65582b55b5c5c2a7b2a1bcd8e59df80da103f1&)

  #### Sequence Number 5

  Dari filter diatas didapatkan Sequence Numbernya adalah **143714** dan RAW Sequence Numbernya adalah **3332725699**
  

  ### Soal Nomor 6 TCP

  Consider the TCP segment containing the HTTP “POST” as the first segment in the data transfer part of the TCP connection
  - At what time was the first segment (the one containing the HTTP POST) in the data-transfer part of the TCP connection sent ?  
  - At what time was the ACK for this first data-containing segment received ? 
  - What is the RTT for this first data-containing segment ? 

  ### Jawaban Nomor 6 TCP

  #### Filtering 6 TCP

  Masukkan filter yang sama dengan nomor 1 `http.request.method == "POST"` pada display filter. Filter tersebut hanya akan menampilkan packet dengan protocol HTTP dan memiliki metode POST
  
  #### Arrival Time 6

  ![No6](https://cdn.discordapp.com/attachments/773324309020147732/1162599950446768168/image.png?ex=653c8694&is=652a1194&hm=f4abe637bfa329991b891870051e5833c006f71b84a64965cadb4f505ad9a4f0&)

  Didapatkan bahwa Arrival Time dari data di packet tersebut adalah pada **Oct 14, 2023 07:44:36.358566**

  #### Receiving Time 6

  Setelah itu lihat packet responsenya 

  ![No6-1](https://cdn.discordapp.com/attachments/773324309020147732/1162602544724451348/image.png?ex=653c88fe&is=652a13fe&hm=a86a2f82c013451af2fc84fad2f6f7a70bb96fa26d80fd9a2965cb8a5165fd10&)

  Didapatkan bahwa Receiving Time dari data yang tadi di POST adalah pada **Oct 14, 2023 07:44:36.63477**

  #### RTT First Segment 6

  Sehingga dari dua informasi diatas bisa didapatkan bahwa RTT atau Round Trip Time dari data yang di POST adalah **0.276204 s**


  ### Soal Nomor 7 TCP

  What is the length (header plus payload) of each of the first four data-carrying TCP segments ?
    
  ### Jawaban Nomor 7 TCP

  #### Filtering 7 TCP

  Masukkan filter yang sama dengan nomor 1 `http.request.method == "POST"` pada display filter. Filter tersebut hanya akan menampilkan packet dengan protocol HTTP dan memiliki metode POST

  #### First Frame Length 7

  ![No7](https://cdn.discordapp.com/attachments/773324309020147732/1162601533221908510/image.png?ex=653c880d&is=652a130d&hm=5a5377e7e6022cec49e8c7e5385ee46d8e162e27df9c12d7dbdc58805cda6f41&)

  Didapatkan bahwa frame length dari packet diatas adalah **9328 bytes (74624 bits)**

  #### Second Frame Length 7

  Kemudian pilih packet response POST nya 

  ![No7-1](https://cdn.discordapp.com/attachments/773324309020147732/1162602074794627083/image.png?ex=653c888e&is=652a138e&hm=14f4e81ae5b912b56b6694bfe3784d7dbf6fe756fa9beee1c5ca0d93dbd76fde&)

  Didapatkan bahwa second frame lengthnya adalah **831 bytes (6648 bits)**

  
  ## UDP

  ### Soal Nomor 1 UDP

  Select the first UDP segment in your trace
  - What is the packet number of this segment in the trace file ?
  - What type of application-layer payload or protocol message is being carried in this UDP segment ?
  - How many fields are there in the UDP header ?

  ### Jawaban Nomor 1 UDP

  #### Filtering 1 UDP 

  Masukkan filter  `UDP` pada display filter dan pilih packet teratas

  ![No8](https://cdn.discordapp.com/attachments/773324309020147732/1162603603165446236/image.png?ex=653c89fb&is=652a14fb&hm=365abfec0084892b50a2428356063f67e003eda9af5c6b7bb3adfcacf927fcd2&)

  #### Packet Number 1

  Dari filter diatas, didapatkan bahwa packet numbernya adalah **5**

  #### Application Layer Payload

  Dari filter diatas juga, didapatkan bahwa info packetnya adalah **62426 -> 443 len = 29** yang mana artinya paket UDP pertama memiliki source port 62426, destination port 443, dan panjang sebesar 29. Destination port 443 adalah port yang umumnya digunakan untuk protokol HTTPS (Hypertext Transfer Protocol Secure), yang digunakan untuk pengiriman data melalui koneksi yang aman dan terenkripsi. Ini adalah protokol yang sering digunakan untuk mengakses situs web melalui HTTPS.

  #### UDP Header 1

  Dari filter diatas, didapatkan juga bahwa UDP Header yang ada pada packet tersebut berjumlah **4**, yaitu Source Port, Destination Port, Length, dan Checksum


  ### Soal Nomor 2 UDP

  By consulting the displayed information in Wireshark’s packet content field for this packet (or by consulting the textbook), what is the length (in bytes) of each of the UDP header fields ?
  
  ### Explanation 2 UDP

  Masing masing dari UDP Header memiliki panjang 2 bytes, sehingga total panjang UDP Header adalah **8 bytes**


  ### Soal Nomor 3 UDP

  The value in the Length field is the length of what ? (You can consult the text for this answer). Verify your claim with your captured UDP packet.

  ### Explanation 3 UDP
  Nilai field "Length" dalam header UDP mengindikasikan panjang keseluruhan dari segmen UDP, yang mencakup panjang header UDP itu sendiri dan panjang payload data. Dalam konteks protokol UDP, "Length" mengacu pada panjang total segmen UDP dalam byte, termasuk panjang header UDP dan data payload.

  ![No3UDP](https://cdn.discordapp.com/attachments/773324309020147732/1162606455992635393/image.png?ex=653c8ca3&is=652a17a3&hm=789fe6240e1dc8f1c3fbe0084a67915ba2e3bd13891fdcb16e7fb6570c229d4d&)

  Pada detail packet tersebut panjang lengthnya adalah **37**, jika sesuai penjelasan diatas angka tersebut didapat dari total panjang UDP Header ditambah dengan data UDP payload nya yaitu **8 + 29 = 37**


  ### Soal Nomor 4 UDP

  What is the maximum number of bytes that can be included in a UDP payload ? 

  ### Explanation 4 UDP

  Jumlah maksimum byte yang dapat dimasukkan dalam sebuah payload UDP adalah 65.527 byte. UDP memiliki field 16-bit untuk panjang payload, yang berarti dapat merepresentasikan nilai dari 0 hingga 65.535 (2^16 - 1). Namun, header UDP itu sendiri memiliki panjang 8 byte. Oleh karena itu, ukuran payload maksimum adalah 65.535 - 8 = 65.527 byte. Ini adalah jumlah maksimum data yang dapat dibawa dalam payload sebuah paket UDP tunggal.


  ### Soal Nomor 5 UDP

  What is the largest possible source port number ?
  
  ### Explanation 5 UDP

  Nomor port sumber terbesar yang mungkin dalam konteks protokol lapisan transportasi UDP atau TCP adalah 65.535. Hal ini karena nomor port direpresentasikan dengan 16 bit, yang memungkinkan nilai dari 0 hingga 65.535 (2^16 - 1). Nomor port digunakan untuk mengidentifikasi endpoint komunikasi yang berbeda pada sebuah host, dan mereka adalah bagian integral dari addressing dalam komunikasi jaringan.


  ### Soal Nomor 6 UDP

  What is the protocol number for UDP ?
  
  ### Explanation 6 UDP

  Nomor protokol untuk UDP adalah 17 dalam notasi desimal. Anda dapat menemukan nomor protokol ini dalam field "Protocol" (Protokol) dalam datagram IP yang mengandung segmen UDP yang ingin Anda analisis. Field "Protocol" mengidentifikasi protokol transportasi yang digunakan dalam datagram IP tersebut, dan dalam konteks UDP, nilainya adalah 17 dalam notasi desimal.


  ### Soal Nomor 7 UDP

  Examine the pair of UDP packets in which your host sends the first UDP packet and the second UDP packet is a reply to this first UDP packet. 
  - What is the packet number of the first of these two UDP segments in the trace file ?
  - What is the packet number of the second of these two UDP segments in the trace file ?
  - Describe the relationship between the port numbers in the two packets.

  
  ### Jawaban Nomor 7 UDP

  #### First Packet Number

  Seperti filter pada nomor 1 UDP, nomor packet pertama adalah **5**

  #### Second Packet Number

  Masih menggunakan filter yang sama, nomor packet kedua adalah **6**

  #### Explanation 7 UDP

  Source port first packet : 192.168.0.108
  Destination port first packet : 142.251.12.138
  Source port second packet : 142.251.12.138
  Destination port second packet : 192.168.0.108
  Relation :  Dalam konteks respon UDP, source port segmen pertama akan menjadi destination port segmen kedua, yang mengindikasikan bahwa segmen kedua adalah respons atas permintaan segmen pertama.


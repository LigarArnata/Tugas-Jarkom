# Tugas Hands On TCP dan UDP Jarkom

![Lambang ITS](https://www.its.ac.id/wp-content/uploads/2020/07/Lambang-ITS-2-320x320.png)

- Ligar Arsa Arnata (5025211244)

## Daftar isi

- [Tugas Hands On TCP dan UDP Jarkom](#tugas-hands-on-tcp-dan-udp-jarkom)
  - [Daftar Isi](#daftar-isi)
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
      - [Filtering](#filtering-3-tcp)
      - [RAW Sequence Number](#raw-sequence-number-3)
    - [Soal Nomor 4](#soal-nomor-4-tcp)
      - [Filtering](#filtering-4-tcp)
      - [SYNACK Segment](#synack-segment-4)
      - [Acknowledgement Field](#acknowledgement-field-4)
      - [Explanation](#explanation-4-tcp)
    - [Soal Nomor 5](#soal-nomor-5-tcp)
      - [Filtering](#filtering-5-tcp)
      - [Sequence Number](#sequence-number-5)
      - [RAW Sequence Number](#raw-sequence-number-5)
    - [Soal Nomor 6](#soal-nomor-6-tcp)
      - [Filtering](#filtering-6-tcp)
      - [Arrival Time](#arrivel-time-6)
      - [Receiving Time](#receiving-time-6)
      - [RTT First Segment](#rtt-first-segment-6)
    - [Soal Nomor 7](#soal-nomor-7-tcp)
      - [Filtering](#filtering-7-tcp)
      - [First Frame Length](#first-frame-length-7)
      - [Second Frame Length](#second-frame-length-7)
  - [UDP](#udp)
    - [Soal Nomor 1](#soal-nomor-1-udp)
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
      - [First Packet Number](#first-packet-number-7)
      - [Second Packet Number](#second-packet-number-7)
      - [Explanation](#explanation-7-udp)



  ## TCP

  ### Soal Nomor 1 TCP

  What is the IP address and TCP port number used by the client computer (source) that is transferring the alice.txt file to gaia.cs.umass.edu?

  ### Jawaban Nomor 1 TCP


  ### Soal Nomor 2 TCP

  What is the IP address of gaia.cs.umass.edu? On what port number is it sending and receiving TCP segments for this connection ?
  
  ### Jawaban Nomor 2 TCP


  ### Soal Nomor 3 TCP

  What is the sequence number of the TCP SYN segment that is used to initiate the TCP connection between the client computer and gaia.cs.umass.edu ?

  ### Jawaban Nomor 3 TCP


  ### Soal Nomor 4 TCP

  - What is the sequence number of the SYNACK segment sent by gaia.cs.umass.edu to the client computer in reply to the SYN ?
  - What is it in the segment that identifies the segment as a SYNACK segment ?
  - What is the value of the Acknowledgement field in the SYNACK segment ?
  - How did gaia.cs.umass.edu determine that value ?

  ### Jawaban Nomor 4 TCP


  ### Soal Nomor 5 TCP

  What is the sequence number of the TCP segment containing the header of the HTTP POST command ?
  
  ### Jawaban Nomor 5 TCP


  ### Soal Nomor 6 TCP

  Consider the TCP segment containing the HTTP “POST” as the first segment in the data transfer part of the TCP connection
  - At what time was the first segment (the one containing the HTTP POST) in the data-transfer part of the TCP connection sent ?  
  - At what time was the ACK for this first data-containing segment received ? 
  - What is the RTT for this first data-containing segment ? 

  ### Jawaban Nomor 6 TCP


  ### Soal Nomor 7 TCP

  What is the length (header plus payload) of each of the first four data-carrying TCP segments ?
    
  ### Jawaban Nomor 7 TCP



  ## UDP

  ### Soal Nomor 1 UDP

  Select the first UDP segment in your trace
  - What is the packet number of this segment in the trace file ?
  - What type of application-layer payload or protocol message is being carried in this UDP segment ?
  - How many fields are there in the UDP header ?

  ### Jawaban Nomor 1 UDP


  ### Soal Nomor 2 UDP

  By consulting the displayed information in Wireshark’s packet content field for this packet (or by consulting the textbook), what is the length (in bytes) of each of the UDP header fields ?
  
  ### Jawaban Nomor 2 UDP


  ### Soal Nomor 3 UDP

  The value in the Length field is the length of what ? (You can consult the text for this answer). Verify your claim with your captured UDP packet.

  ### Jawaban Nomor 3 UDP


  ### Soal Nomor 4 UDP

  What is the maximum number of bytes that can be included in a UDP payload ? 

  ### Jawaban Nomor 4 UDP


  ### Soal Nomor 5 UDP

  What is the largest possible source port number ?
  
  ### Jawaban Nomor 5 UDP


  ### Soal Nomor 6 UDP

  What is the protocol number for UDP ?
  
  ### Jawaban Nomor 6 UDP


  ### Soal Nomor 7 UDP

  Examine the pair of UDP packets in which your host sends the first UDP packet and the second UDP packet is a reply to this first UDP packet. 
  - What is the packet number of the first of these two UDP segments in the trace file ?
  - What is the packet number of the second of these two UDP segments in the trace file ?
  - Describe the relationship between the port numbers in the two packets.

  
  ### Jawaban Nomor 7 UDP

{\rtf1\ansi\ansicpg1252\cocoartf2820
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww24980\viewh15040\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 \

\fs72 kQUIC: A Kernel-based QUIC Transport for IoT\
\

\fs36 This project is developed in SIOTLAB in Santa Clara University by Puneet Kumar (PhD student) under professor Behnam Dezfouli. \
Since kernel size is too big, the touched files are in their respective folders.\
\

\fs48 Installing the kernel:\

\fs36 - Clone the Linux source.\
- Modify the make file to compile the quic related files.\
- Compile and install the linux.\
\

\fs48 Usage:\

\fs36 - Socket type is IPPROTO_QUIC, and socket opening is normal procedure just like UDP or TCP socket.\
- Write and read system calls just works normally.\
- Associated the above msghdr struct with the socket APIs for application multiplexing.\
\

\fs48 For ancillary data use:\

\fs36 - struct msghdr *msg and cmag_type is the field which will be application ID.\
\
\

\fs48 Hierarchy:\

\fs36 \
main tree:\
|\
|----include\
|       |\
|       |-- net\
|       |-- uapi\
|\
|----net\
|      |\
|      |--ipv4\
|      |--netfilter\
  \

\fs72 \
}
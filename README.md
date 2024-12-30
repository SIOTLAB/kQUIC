# **kQUIC: A Kernel-based QUIC Transport for IoT**

Welcome to the **kQUIC** project! This kernel-based QUIC transport protocol is tailored for IoT environments and was developed in **SIOTLAB** at Santa Clara University by **Puneet Kumar (Ph.D. student)** under the guidance of **Professor Behnam Dezfouli**.

## **Overview**
The kQUIC project enhances the **Linux kernel** to integrate QUIC as a transport protocol, making it suitable for IoT systems. The implementation provides efficient handling of QUIC connections directly within the kernel, enabling robust and high-performance networking for IoT applications.

---

## **Features**
- **QUIC in the Kernel:** Implements QUIC as a native transport protocol using `IPPROTO_QUIC`.
- **Seamless Integration:** Supports standard socket operations (`read`, `write`, `msghdr` struct association).
- **Application Multiplexing:** Provides enhanced support for application ID management through ancillary data (`struct msghdr *msg` and `cmag_type` fields).

---

## **Project Structure**
```
main tree:
|
|----include
|       |
|       |-- net
|       |-- uapi
|
|----net
|      |
|      |-- ipv4
|      |-- netfilter
```

---

## **Installation**

### **Step 1: Clone the Linux Source**
```bash
git clone https://github.com/torvalds/linux.git
```

### **Step 2: Modify and Compile the Kernel**
1. Add the necessary QUIC-related files to the source tree.
2. Update the **Makefile** to include the QUIC implementation.
3. Compile the kernel:
   ```bash
   make -j$(nproc)
   sudo make modules_install
   sudo make install
   ```

### **Step 3: Boot into the New Kernel**
Reboot your system and select the newly compiled kernel.

---

## **Usage**
1. **Socket Operations:**
   - Use `IPPROTO_QUIC` as the protocol type during socket creation.
   - Socket operations (`read` and `write`) function similarly to UDP or TCP sockets.

2. **Application Multiplexing:**
   - Associate the `msghdr` struct with the socket APIs to manage application-specific data.

3. **Ancillary Data Handling:**
   - Use `struct msghdr *msg` and the `cmag_type` field to specify the application ID.

---

## **Contributing**
We welcome contributions to enhance and optimize kQUIC! Please submit a pull request or open an issue to discuss your ideas.

---

## **Acknowledgments**
Developed by **Puneet Kumar**, Santa Clara University, under the mentorship of **Professor Behnam Dezfouli** at **SIOTLAB**.

---

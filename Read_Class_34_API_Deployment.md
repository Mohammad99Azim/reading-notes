# API Deployment

## SSH

#### What Is SSH?

SSH, or Secure Shell Protocol, is a remote administration protocol that allows users to access, control, and modify their remote servers over the internet.


#### How Does SSH Work

- **Windows:** 
Downloadthe latest version of PuTTY SSH from the [official](https://www.putty.org/) website. After that, install it on your computer. It’s as simple as that.

- **Linux:** 
Most people use the preinstalled OpenSSH on Linux, however, PuTTY on Linux is used more for debugging, connecting to serial ports, and to raw sockets.

On Debian, use the following command:

``sudo aptitude install putty``

Followed by the tools installation command:

``sudo aptitude install putty-tools``




#### Understanding Different Encryption Techniques

The significant advantage offered by SSH over its predecessors is the use of encryption to ensure a secure transfer of information between the host and the client. Host refers to the remote server you are trying to access, while the client is the computer you are using to access the host. There are three different encryption technologies used by SSH:

- Symmetrical encryption
- Asymmetrical encryption
- Hashing



#### Conclusion

Gaining an in-depth understanding of the underlying how SSH works can help users understand the security aspects of this technology. Most people consider this process to be extremely complex and un-understandable, but it is much simpler than most people think.

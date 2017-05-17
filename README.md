# MS17-010
As all of our research is now in Metasploit master repository, there was no reason to confuse everyone by keeping this repository open as there were two versions of everything and due to overwhelming popularity support became a nightmare as this is merely a side project. **Please do not make support issues here, as they will not be answered.**

Those searching for the scanners:

- Metasploit: https://www.rapid7.com/db/modules/auxiliary/scanner/smb/smb_ms17_010
- Python: https://github.com/nixawk/labs/blob/master/MS17_010/smb_exploit.py

Those searching for EternalBlue:

- https://www.rapid7.com/db/modules/exploit/windows/smb/ms17_010_eternalblue

This version disproved the robustness of most existing IDS rules (at the time). Those looking to make IDS rules should look at the final SMB1 Trans2 packet. These contain fixed offsets, however it may be possible to use other addresses. However, the hole in which those offsets lie must always be laid out in a similar manner. There is also the pattern of several SMB2 groom requests will null headers and shellcode.

Windows kernel shellcode will be in Metasploit as well as submitted to exploit-db when x86 version is completed.

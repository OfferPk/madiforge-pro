\# MADIForge Pro (v1.0.0)  
\> \*\*AES10 / MADI Multichannel Audio Digital Interface Engineering Suite\*\*

\---

\#\# Overview  
\*\*MADIForge Pro\*\* is an open-standard engineering studio, frame sizer, and subframe parity validator designed for recording studio engineers, live touring sound operators, and broadcast OB truck technicians managing high-density multichannel audio over 75-ohm BNC coaxial cable and multimode optical fiber.

\#\#\# Normative Standards Covered:  
\- \*\*AES10-2008 (MADI):\*\* Multichannel Audio Digital Interface serial transmission.  
  \- Channel Modes: 64-channel mode (standard 48 kHz), 56-channel mode (legacy with \+-12.5% varispeed), 32-channel mode (96 kHz SMUX), 16-channel mode (192 kHz SMUX).  
  \- Subframe: 32 bits per channel subframe (4-bit preamble/ID, 24-bit audio sample, Validity, User, Channel Status, and Even Parity).  
  \- Physical Layer: NRZI 4B/5B line coding operating at 125.0 Mbaud symbol rate over 75-ohm BNC coax (\<= 100m) or 1300nm FDDI optical fiber (\<= 2km).

\---

\#\# Key Modules  
1\. \*\*MADI Frame Budget & Bandwidth Modeler:\*\*  
   \- Computes unencoded payload data rates (e.g. 98.30 Mbps for 64ch-48k), symbol rates (122.88 Mbaud), and synchronization headroom (1.7% to 14.0%).  
   \- Calculates transmission medium distance limits (100m coaxial, 2000m multimode fiber).  
2\. \*\*64-Channel Audio Stream Canvas:\*\*  
   \- Visual audio raster rendering all 64 channels with real-time level indicators.  
3\. \*\*Subframe Assembler & Even Parity Validator:\*\*  
   \- Validates bit 31 even parity calculation across audio, validity, user, and channel status bits.  
4\. \*\*10-Point Normative AES10 Protocol Auditor:\*\*  
   \- Pre-flight compliance validator verifying 125 Mbaud symbol rate, 32-bit subframes, channel 0 block start markers, cable limits, and varispeed tolerances.  
5\. \*\*Standalone Python 3 CLI Suite:\*\*  
   \- \`build/madi-cli.py\`: Production CLI with JSON output for automated broadcast pipeline verification.

\---

\#\# Automated Verification  
Run the unit test suite:  
\`\`\`bash  
python3 test\_madi.py  
\`\`\`  
\*Result: 10/10 unit tests passed (100% pass rate).\*

\---

\#\# License  
Commercial Proprietary License (v1.0.0). Built for Broadcast & Recording Studio Audio Engineers.  

# Social Engineering: OSINT, Phishing & Sniffer Detection

A hands-on project from my cybersecurity training covering three areas of
social engineering and the attacks around it: open-source intelligence,
phishing, and account hijacking via network sniffing. The goal was to see
how attackers gather information and manipulate people, and how
organizations can defend against it.

> Note: the result files in this repository are written in Russian.
> This README summarizes them in English.

## Tasks

### 1. OSINT: Locating Places from Photos
Identified the country, region, town and extra details for five photos
using open sources only. Results are in `task1_osint/I_am_osinter.txt`.
- **Techniques:** reverse image search, landmark and architecture
  recognition, road signs and street furniture, map cross-checking
- **Results:** located all five photos: an abandoned village by a
  reservoir in Aragon (Spain), a residential street in Russia (location
  given as a best estimate, since I could not confirm it independently),
  a suburb of Paris (France), a lighthouse on the southern tip of
  Sardinia (Italy), and a volcanic crater lake in East Java (Indonesia)
- **Takeaway:** small details like a bell tower, a road sign or a fire
  hydrant are often enough to place a photo, and that is exactly what
  makes employees' public photos risky

### 2. Phishing: Awareness-Training Email
Wrote a fictional phishing email for security-awareness training, asking
a colleague to arrange a temporary office pass. All names are invented.
Final email: `task2_phishing/email_for_you.md`.
- **Indicators used:** urgency (a one-hour deadline), appeal to status
  (acting on the director's instruction), and fake peer cooperation (a
  colleague who supposedly helped before)
- **AI-assisted workflow:** drafted with an AI assistant, then edited and
  tested for realism by me. The full dialogue, with my comments on what I
  kept and changed, is in `task2_phishing/ai_task2_dialogue.txt`.

### 3. Sniffer Detection in a Wi-Fi Traffic Dump
Analyzed a capture of 802.11 traffic (211 frames) to find the MAC address
of a device passively sniffing the network.
- **Tools:** Wireshark / tshark
- **Result:** identified the sniffer as `11:22:33:44:55:66`. It sends
  probe requests but never appears as a receiver in any frame, unlike
  the other four devices, which both send and receive data. So it
  listens to the air without taking part in the actual exchange.
- **Files:** `task3_sniffing/sniffer_detector.txt` (answer and reasoning)
  and `task3_sniffing/ai_task3_dialogue.txt` (how I used AI as a
  consultant while doing the analysis myself)

## Key Takeaways
- OSINT is very hard to defend against; employee awareness is the main
  control
- Phishing works by exploiting trust, urgency and authority rather than
  technical flaws
- Sniffers can often be spotted by behavior: they listen but do not
  take part in conversations

## Disclaimer
All content is for educational purposes. Names, addresses and scenarios
in the phishing email are fictional.

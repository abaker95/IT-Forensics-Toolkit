# Digital-Forensics-Toolkit

## Volatility

This tool is used to analyze volatile memory extracts. This tool is most effective when it is adapted to work for extracting memory from a specific operating system. The memory extract for Linux can happen with a tool such as LiME. Volatility can be loaded with different profiles to pull out different types of data for the querying user. An example of this PSlists.
Volatility supports indexing processes, dynamic linked libraries (DLLs), the Windows registry, kernel memory, and network connections. Each of these indexes can provide a forensic investigator with deeper understanding of what the user or attacker was doing on the device. Volatility can be a great help to investigators, the only time I would not recommend using this tool is if the target operating system is not supported.

Location for retrieving tool: <https://github.com/volatilityfoundation/volatility>

Command reference for Volatility: <https://github.com/volatilityfoundation/volatility/wiki/Command-Reference>

Basic tutorial for installing and running Volatility: <https://www.howtoforge.com/tutorial/how-to-install-and-use-volatility-memory-forensic-tool/>

## Write Blocker

This is a piece of hardware that can be used to acquire a copy of a seized hard drive. Then using a tool like FTK Imager, a copy can be saved to disk. This copy can then be hashed to show that it has not changed from the original.
I would recommend this piece of hardware because it has been built to prevent the reading operating system from writing any new data to the seized device. I do not have any brands that should be preferred over another. Be ready to wait as the acquisition happens. The bigger the drive, the longer the wait.

Follow this link for a tutorial of using FTK Imager with a Write blocker: <https://digital-forensics.sans.org/blog/2009/06/18/forensics-101-acquiring-an-image-with-ftk-imager/>

## FTK Imager

FTK short for Forensic Tool Kit is a suite of digital forensic tools for acquiring and analyzing a device for a case. This is a proprietary tool develped by Access Data.
I have only used FTK Imager to copy a hard drive. It did a great job doing this. I know this is only a small piece of what the whole tool kit is designed to do. FTK Imager would be a great tool to invest in if digital forensics is often necessary for a business. If this is not a common occurance, I would recommend sticking to forensically sound and approved open source tools.

Main page for FTK Imager: <https://accessdata.com/products-services/forensic-toolkit-ftk>

## Rekall

Rekall is a memory analysis framework that targets volatile memory. It is similar in function to Volatility. Rekall can be used to acquire, analyze, and report on memory findings. It has several tools that can be used to aid in each of those focuses of the framework itself.
I have only used Rekall's OSXpmem tool to acquire the volatile memory from an Apple Imac. This is a simple tool that can be loaded onto a flash drive. I would recommend this approach to prevent the loss of any volatile memory in the process of retrieiving and installing the tool locally on the device that is seized. Also, make sure the tool has the correct file permissions when moved onto the flash drive.

Rekall Homepage: <http://www.rekall-forensic.com/>

Rekall guide: <http://www.rekall-forensic.com/documentation-1/rekall-documentation/tutorial>

## Autopsy

After hard drive acquisition, Autopsy can be utilized to reassemble the persistent memory. Data can be extracted and examined for further detail and analysis regarding a security incident or investigation. Autopsy has several features to aid an investigator in a case. Some of these features include Registry Analysis using RegRipper, timeline analysis to graphically identify activity, and web artifacts to see user web activity. 
I like that Autopsy is open source and allows you to begin searching through files before they have been processed fully by the software. Autopsy supports global searches and can save an investigators time by organizing common fields of interest into sub categories of navigation. I liked how intuitive the tool was to use the first time I used it.

Here is a link to Autopsy’s main page: <https://sleuthkit.org/index.php>

## Snort

This is a signature-based network intrusion detection system. It takes in rules and logs alerts that are triggered when an event hits a given threshold. It scales well and primarily works for monitoring networks.
I like Snort IDS because it allows a security professional to scale their work. Pcaps are good for small isolated instances, but they do not scale well. Pcaps contain huge amounts of data and log entries that an analyst or forensic investigator can get overwhelmed and burnt out sifting through them. Snort solves these problems if a security engineer can create effective rules to utilize Snort’s computing resources.
Snort will require you to register an account with them on your first initial download of the software. You can also subscribe to their email list to stay in the know when new features or rule sets are added. This tool will take practice to adapt the rules to a custom network.

Snort IDS homepage: <https://www.snort.org/>

Guide to setting up Snort configuration: <https://null-byte.wonderhowto.com/how-to/hack-like-pro-snort-ids-for-aspiring-hacker-part-2-setting-up-basic-configuration-0169711/>

## Wireshark

Wireshark is a GUI for searching through network Pcap files. It has powerful filtering capabilities. Wireshark is very versatile in how it can be used. It is often used to diagnose and troubleshoot issues in a network. For a forensic investigator it can be utilized to search through traffic acquired from a mirror port and help in network forensic analysis.
The best advice I can give on using Wireshark effectively is understand network protocols before you start sifting through them. This understanding can aid also give you good insights into correlating the network traffic with malicious intent. Remember that the bigger the Pcap file the longer it will take for Wireshark to filter all that data.

Wireshark homepage: <https://www.wireshark.org/>

Using Wireshark for forensics: <https://resources.infosecinstitute.com/wireshark-open-source-forensic-tool/#gref>

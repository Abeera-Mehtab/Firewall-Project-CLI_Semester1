Firewall in C++
Overview
This project implements a basic firewall application in C++. The program processes traffic based on a set of rules provided in a specific format. It determines whether to allow or deny the traffic based on these rules and logs the results in a DAT file, which is then displayed in the CLI.

Features
	• Reads firewall rules from a text file.
	• Processes traffic data from a text file.
	• Matches traffic against rules to allow or deny access.
	• Outputs results to a DAT file in a specified format.
	• Displays the processed results in the command-line interface.

File Descriptions
Input Files:
	1. Rules File: Contains rules in the following format:
[RULE NO] [FIELD] [VALUE] [DECISION]
		○ RULE NO: Unique identifier for the rule.
		○ FIELD: The traffic field to match (e.g., SRC, DST, PRO).
		○ VALUE: The value or range of values to match (e.g., IP address or protocol).
		○ DECISION: ALLOW or DENY.
	2. Traffic File: Contains traffic entries as a single string in the following format:
[SRC:source_IP;DST:destination_IP;PRO:protocol;DATA_IN_HEX_FORMAT][...]
		○ SRC: Source IP address.
		○ DST: Destination IP address.
		○ PRO: Protocol (e.g., TCP, UDP).
Output File:
	• Results File: Outputs the processed traffic results in a DAT file with the following format: 
SRC source_IP    DST destination_IP    PRO protocol    DECISION    RULE_NO

Usage
Command-Line Syntax:
	1. Place the rules and traffic text files in the same directory as the program.
	2. Run the program: 
./firewall rules.txt traffic.txt
		○ rules.txt: File containing the firewall rules.
		○ traffic.txt: File containing the traffic data.
Result Display:
	• The program writes the results to a DAT file.
	• The results are then displayed in the command-line interface.

Project Structure
	• main.cpp: Contains the main logic of the program.
	• rules.txt: Input file with firewall rules.
	• traffic.txt: Input file with traffic data.
	• results.dat: Output file with processed results.
	• README.md: Project documentation.

Dependencies
	• C++11 or later

Compilation
Compile the program using any C++ compiler. For example:
g++ -o firewall source.cpp

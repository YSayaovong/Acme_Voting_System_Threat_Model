# Acme Voting System Threat Model

## Project Overview

This repository contains a threat model designed by Acme Inc. for a voting system contracted by the Government of Norway. The system aims to facilitate secure electronic voting and prevent voter fraud. The threat model analyzes potential security risks using the STRIDE framework and presents a system architecture diagram, data flow, and potential security vulnerabilities.

## Components

The voting system is made up of four components:

1. **Database (MySQL)**: Stores the voting data and other sensitive information. It is secured behind a government firewall, and only the backend server can access it.
2. **Backend Server (Java)**: Facilitates authentication, authorization, and data storage. Handles requests from both voting clients and admin clients.
3. **Admin Client (Java)**: Allows election officials to manage the system, upload measures, and run reports. Two admin levels are supported: 
   - **Election Admin**: Can run election reports.
   - **System Admin**: Can manage user accounts and perform system checks.
4. **Voting Client (Java)**: A portal for citizens to securely vote and verify their votes.

## Data Flow Diagram

The system architecture includes the following data flows:
- **Voting Client ↔ Backend Server**: Authentication and voting data.
- **Admin Client ↔ Backend Server**: Admin actions and report generation.
- **Backend Server ↔ Database**: Secure data storage.

A detailed diagram showing the flow of data and trust boundaries is included in this repository.

## STRIDE Threats

This threat model identifies the following potential risks based on the STRIDE framework:
- **Spoofing**: Attackers may attempt to impersonate valid users or admins.
- **Tampering**: Unauthorized users could try to alter voting data stored in the database.
- **Repudiation**: Malicious actors might deny performing certain actions without proper logging.

## Repository Contents

- **Threat Model Document**: A PDF file containing the full system diagram, data flow, and STRIDE analysis.
- **Source Code**: Java code for the backend server, admin client, and voting client.
- **Diagrams**: Architecture and data flow diagrams for the system.
- **README.md**: This file.

## How to Run the System

1. Set up the MySQL database using the provided SQL scripts.
2. Deploy the Java-based backend server.
3. Launch the Admin Client and Voting Client applications.


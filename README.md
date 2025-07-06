Cypher KeyGen Pro - Password Permutation Engine
![image](https://github.com/user-attachments/assets/d213faf1-5986-4da2-b492-97db0b3a4cc5)

Table of Contents
Introduction

Features

Installation

Usage

Technical Details

Performance Considerations

Ethical Use

License

Introduction
Cypher KeyGen Pro is an advanced password permutation tool designed for ethical security testing and password auditing. This web-based application generates both dictionary-based words and random combinations from input characters, helping security professionals test system resilience against brute-force attacks.

The tool features a hacker-inspired interface with real-time performance warnings, multiple output formats, and comprehensive download options for use with security testing tools.

Features
Core Functionality
Multi-character Input: Accepts alphabetic, numeric, and special characters

Smart Permutation Engine:

Dictionary word generation (370,000+ English words)

Random combination generation

Configurable minimum/maximum length

Character Type Filters: Select which character types to include in generation

Advanced Features
Real-time Performance Warnings:

Visual length indicator (green → red gradient)

Blinking warning icon for dangerous input lengths

Crash risk notifications

Multiple Output Options:

Column view (1-3 columns based on screen size)

Alphabetical sorting

Limited/full result display

Comprehensive Download Options:

TXT files for dictionary words, random combos, or combined results

ZIP archive containing all variations

Process Control:

Kill switch for long-running operations

Progress indicator

Responsive Design
Fully responsive interface for:

Mobile devices

Tablets

Desktop screens

Adaptive column layout based on screen size

Installation
Cypher KeyGen Pro requires no server-side installation. To use it:

Option 1: Use the live version hosted at GitHub Pages

Option 2: Local installation

bash
git clone https://github.com/yourusername/cypher-keygen-pro.git
cd cypher-keygen-pro
# Open index.html in any modern browser
Usage
Basic Operation
Enter characters in the input box (up to 30 characters)

Select character types to include (alphabetic, numeric, special)

Set minimum and maximum length for generated words

Choose output types (dictionary words, random combos, or both)

Click "Execute KeyGen" to generate results

Use download buttons to export results

Advanced Options
Column View: Toggle multi-column display

Alphabetical Sort: Change from default length-based sorting

Full Results: Bypass the 800-result safety limit (use with caution)

Performance Tips
For mobile devices, keep inputs under 10 characters

On desktop, 12 characters is the recommended maximum

Use the kill button if generation takes too long

Technical Details
Architecture
Pure client-side JavaScript application

No server-side dependencies

Uses:

Web Workers for background processing (where available)

JSZip for archive creation

Responsive CSS with modern layout techniques

Dictionary Source
Default dictionary from dwyl/english-words

Fallback to embedded common words if network unavailable

Algorithms
Dictionary Matching: Linear scan with character count verification

Permutation Generation: Optimized backtracking algorithm

Duplicate Prevention: Set-based storage for random combos

Performance Considerations
Input Length Guidelines
Characters	Possible Combinations	Performance Impact
1-7	Up to 5,040	Instant
8-11	Up to 39.9 million	Slight delay
12-15	Up to 1.3 trillion	Significant lag
16+	Over 20 quadrillion	Browser crash risk
Memory Usage
Each additional character increases memory requirements exponentially

Mobile devices have stricter limits (300 results by default)

Ethical Use
Cypher KeyGen Pro is intended for:

Security professionals auditing their own systems

Password strength testing

Educational purposes

Warning: Unauthorized password cracking is illegal in most jurisdictions. Only use this tool on systems you own or have explicit permission to test.

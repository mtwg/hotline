# Hotline

<!-- MDTOC maxdepth:6 firsth1:1 numbering:0 flatten:0 bullets:1 updateOnSave:1 -->

- [Hotline](#hotline)   
   - [Specification](#specification)   
   - [Current Implementation](#current-implementation)   
   - [Twilio API -> Asterisk via Aria](#twilio-api-asterisk-via-aria)   
      - [Strengths](#strengths)   
      - [Weaknesses](#weaknesses)   
      - [Opportunities](#opportunities)   
      - [Threats](#threats)   
   - [Asterisk](#asterisk)   
      - [Strengths](#strengths)   
      - [Weaknesses](#weaknesses)   
      - [Opportunities](#opportunities)   
      - [Threats](#threats)   
   - [FreeSwitch](#freeswitch)   
      - [Strengths](#strengths)   
      - [Weaknesses](#weaknesses)   
      - [Opportunities](#opportunities)   
      - [Threats](#threats)   

<!-- /MDTOC -->

## Specification

- Readily accept inbound collect calls
- Accept calls from international numbers
- Readily configurable
  - Add numbers on the fly (ideally with mobile app)
  - Round robin lists (ideally as random as possible)
  - Obfusicate the identity/numbers of call recipients, outbound calls show as hotline number
  - Save contacts to reuse on lists
  - Be able to update recorded greeting on the fly
  - (Not Required) Dial menu with multiple lists
- Secure and private, ideally
  - SIP trunks will implicitly compromise this.
  - Inbound collect calls from correctional facilities will be implicitly compromised.


## Current Implementation

Our current implementation we've used was what was readily available off the shelf -  Twilio + OpenVBX.



## Twilio API -> Asterisk via Aria

We can simulate the Twilio API against Asterisk using the [aria](https://github.com/ssokol/aria) library.
  - Utilizes the ARI which is faster and more secure than other asterisk interfaces

### Strengths
- Allows us to use any twilio client application almost seamlessly i.e. OpenVBX


### Weaknesses
- Risk of high latency
- Another moving part, more vulnerability
- Only supports e164 numbers (thus no int't calls)
- Caveats of providing incomplete twilio functionality

### Opportunities

### Threats


## Asterisk

### Strengths

### Weaknesses

### Opportunities

### Threats


## FreeSwitch

### Strengths

### Weaknesses

### Opportunities

### Threats

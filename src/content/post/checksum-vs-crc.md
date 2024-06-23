---
title: "Checksum VS CRC"
publishDate: "21 Jun 2024"
description: "--------------------------------------------------"
tags: ["Network"]
---

#### Checksum

XOR checksum is a simple error-detection algorithm commonly used in computer networks and data communication. It operates by performing an XOR operation on each byte of data, creating a running checksum.

#### CRC16 CCITT

A cyclic redundancy check (CRC) is an error-detecting code commonly used in digital networks and storage devices to detect accidental changes to digital data.

A CRC is called an n-bit CRC when its check value is n bits long. For a given n, multiple CRCs are possible, each with a different polynomial. Such a polynomial has highest degree n, which means it has n + 1 terms. In other words, the polynomial has a length of n + 1; its encoding requires n + 1 bits.

The simplest error-detection system, the parity bit, is in fact a 1-bit CRC: it uses the generator polynomial x + 1 (two terms), and has the name CRC-1.

CRC1, CRC16, and CRC32 are commonly used.

The CCITT, which stands for the Comité Consultatif International Téléphonique et Télégraphique (International Telegraph and Telephone Consultative Committee), is a historical organization that was responsible for setting international standards for telecommunications.

※ Polynomial representations :
![21](@/assets/21.svg)
<!--- @file
  apple-t2.md for Understanding the UEFI Secure Boot Chain

  Copyright (c) 2019, Intel Corporation. All rights reserved.<BR>

  Redistribution and use in source (original document form) and 'compiled'
  forms (converted to PDF, epub, HTML and other formats) with or without
  modification, are permitted provided that the following conditions are met:

  1) Redistributions of source code (original document form) must retain the
     above copyright notice, this list of conditions and the following
     disclaimer as the first lines of this file unmodified.

  2) Redistributions in compiled form (transformed to other DTDs, converted to
     PDF, epub, HTML and other formats) must reproduce the above copyright
     notice, this list of conditions and the following disclaimer in the
     documentation and/or other materials provided with the distribution.

  THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR
  IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
  MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO
  EVENT SHALL TIANOCORE PROJECT  BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
  SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
  PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
  OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
  WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
  OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF
  ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

-->

## Apple T2 {#apple-t2}

Apple developed [T2](https://www.apple.com/mac/docs/Apple_T2_Security_Chip_Overview.pdf) security chip. _“It features a Secure Enclave coprocessor, which provides the foundation for APFS encrypted storage, secure boot, and Touch ID on Mac.”_

The T2 macOS secure boot chain is similar to other secure boot solution. The chip executes code from immutable Boot ROM as root-of-trust. Then the Boot ROM verifies the iBoot bootloader. The later verifies the T2 kernel, which subsequently verifies the UEFI firmware.

Figure 4-12 shows the T2 macOS Secure Boot chain.

![](/media/image26.png)

###### Figure 4-12: T2 macOS Secure Boot(source: “[Apple T2 Security Chip Overview](https://www.apple.com/mac/docs/Apple_T2_Security_Chip_Overview.pdf)”){#4-12-t2-macOS-secure-boot}

<!--- @file
  tcg-dice.md for Understanding the UEFI Secure Boot Chain

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

## TCG DICE {#tcg-dice}

Different with traditional personal computer, server or mobile, the new segment such as Internet-of-Thing world may have differnt requirment on security. For example, the Trusted Platform Module (TPM) is not feasible for the device in the IoT space. In order to address these special need for IoT, Microsoft defines [Robust IoT](https://www.microsoft.com/en-us/research/wpcontent/uploads/2016/06/RIoT20Paper-1.1-1.pdf) (RIoT). RIoT is an architecture for providing foundational trust services to computing devices. The trust services include device identity, sealing, attestation, and data integrity. Later the name of RIoT is changed to [Device Identifier Composition Engine](https://trustedcomputinggroup.org/work-groups/dice-architectures/) (DICE) and it becomes a standard in Trusted Computing Group (TCG).

DICE is the new root of trust for measurement and foundational security for IoT and any system. Figure 4-14 shows the DICE architecture.

![](/media/image28.png)

###### Figure 4-14: DICE Architecture (source: “[Foundational Trust for IoT and Resource Constrained Devices](https://trustedcomputinggroup.org/resource/foundational-trust-iot-resource-constrained-devices/)”){#4-14-dice-architecture}

DICE starts at power on and has access to unique device secret (UDS). Then easy layer computes secret for the next layer using a one-way function and a measurement of the next layer.  Figure 4-15 shows the DICE boot flow.

![](/media/image29.png)

###### Figure 4-15: DICE Boot Flow (source: “[Foundational Trust for IoT and Resource Constrained Devices](https://trustedcomputinggroup.org/resource/foundational-trust-iot-resource-constrained-devices/)”){#4-15-dice-boot-flow}

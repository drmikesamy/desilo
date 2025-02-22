# Desilo - A Secure Protocol for Fetching Siloed Patient Notes

As a junior doctor, I often faced the critical task of treating elderly patients who couldn't provide a reliable medical history in the middle of the night. With no family to call, no local records, and a closed GP surgery, the risk of missing life-saving medication was high. This struggle to piece together scattered and fragmented patient information is a challenge faced by clinicians worldwide. Desilo aims to solve this by securely fetching and sharing essential patient notes between hospital sites, providing a vital picture for healthcare providers.

<img src="Resources/diagram.png">(https://github.com/drmikesamy/desilo/tree/main/Resources/diagram.png)

Desilo is a simple and open protocol designed to securely fetch siloed patient notes between hospital sites using interoperability standards. It leverages a central authentication and authorisation provider, end-to-end encryption and signatures to ensure data security and integrity, and is built to be resilient without relying on any central trusted server which can be compromised, leading to the catastrophic data breaches we often see in the news, even from reputable companies.

The Desilo Protocol is inspired by the Nostr Protocol, but has been modified in order to meet the the data security and regulatory requirements of healthcare.

## How it works

The concept is straightforward: each hospital site can publish vital patient Note-Summaries, like the last x appointments, pending investigations, current drug regime, past medical history, or allergies, to their own, or another care provider's DCache that can be instantly deployed with very little setup, cost, complexity, tailoring, or overhead. These servers simply perform two functions: store messages and accept authenticated requests. Healthcare providers at different sites can connect to and make requests (containing filter parameters) from these DCaches to securely fetch the required patient notes. The protocol defines the messages exchanged between clients and DCaches to publish and fetch patient notes securely.

DCaches can be hosted on-site, delegated to cloud providers like Azure or AWS controlled by the care setting, or outsourced to a third-party supplier. Each care setting can also publish Note-Summaries to the DCaches run by other care providers, depending on the rules set by the provider, if they are perhaps smaller and don't have the technical know-how. The intention is to create a secure, low-risk, cost-effective, access-controlled layer for the sharing of vital patient data.

The two central components of the Desilo network are the Authorisation Service, which is a secure registry of care provider identities and authorisation levels, and the Locator Service, which tracks Note-Summaries by ID (a 32-bit unique hex string), maps each ID to a DCache.

Public-key cryptography is used to sign each patient Note-Summary, which adds a digital signature of the authorized individual and care setting, ensuring the integrity and authenticity of the patient notes. When a healthcare provider requests Note-Summaries, they must also provide a JWT access token to both authenticate to the DCache and prove they have the correct authority to access Note-Summaries for a given patient.

## Protocol specification

For detailed information about the protocol, you can refer to the Desilo Improvements [DIPs] which outline the technical details and message formats used in Desilo. To contribute, simply raise a merge/pull request with your proposed DIP.

## Getting started

Our goal is for Desilo to be the product of many minds across disciplines and will evolve as various contributors submit DIPs and the Desilo Protocol Specification set develops.

## Licence

Desilo is licenced under the MIT Licence.
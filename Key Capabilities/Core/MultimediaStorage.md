# Multimedia Storage Capability

## Diagram
![MultimediaStorageCapability](https://raw.githubusercontent.com/TheMarmots/ArchKatas2022/main/assets/MultimediaStorageCapability.svg)

## Description
The multimedia storage capability is broadly responsible for handling downloadable readable content of an offering. This service also connects to the auth capability microservice to get role/user information to validate request to pdfs.

## Use Cases
* Upload resources
* Download/fetch resources
* Handling errors

## Components
* Multimedia Storage Capability: Logic to communicate with object store, handle upload and download/fetch requests
* Object storage: An object store for readable content in the form of pdfs.

## Architectural Characteristics
* Low cost
* Availability

## ADR
- [ObjectStorage](../../ADRs/ObjectStorage.md)

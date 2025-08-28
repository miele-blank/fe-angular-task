# Angular web app assessment task

## Context

You are tasked with building a web application for a launderette service that allows 
users to plan and pay for their laundry processes. The frontend Angular app will interact with a RESTful 
backend API that manages washing and drying cycles, devices, and pricing.

A mock version of the backend API is provided as `backend-api.json`, which can be run locally using json-server.

## Backend API overview

The backend application is responsible for managing
all processes, especially control the devices remotely to start or stop a program. 

It exposes the following key resources:

- `Cycle`: Represents an active or past washing/drying process started by an user 
  using a real device.
  The attributes of a cycle like `status`, `stoppedAt` and `invoiceLines` change during 
  life-cycle of a cycle instance and represent the current process details. The backend
  application manages the cycle process logic in the background, in dependency to user actions or device status. 
- `Tariff`: Represents pricing information associated with a device and used for invoicing.
- `Device`: Represents a physical washer or dryer available for use.

The frontend should consume this API to display and manage laundry operations.

## Task requirements

**Your Angular application should:**

- Be buildable and runnable via NPM/Yarn from the command line or a common IDE.
- Be usable locally from a browser
- Consume the provided REST API to fetch and update data.
- Display a list of cycles, both active and past, with relevant details:
  - Status (e.g., running, completed)
  - Start/stop times
  - Associated device and tariff
  - Invoice details
- Allow users to start a new cycle by selecting an available device (washer or dryer).


**Optional enhancements:**

- UI/UX aligned with Miele MOVE https://www.miele-move.com
- Unit or integration tests ensuring regression of the web app
- Any other creative feature or improvement — surprise us!

## Deliverables

- Source code provided via:
  - Archive file (preferred)
  - GitHub repository
- A brief README.md including:
  - Setup instructions (install, build, run)
  - Any assumptions or notes
  - Description of optional features implemented

## How to start the example REST mocks locally

- Install [json-server](https://github.com/typicode/json-server)
  - Run `npm install json-server`
- For starting mock `API`:
  - Run `npx json-server backend-api.json`
  - Access the API endpoints from http://localhost:3000/


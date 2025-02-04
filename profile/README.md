# Waterstones Application Architecture

This repository provides an overview of the Waterstones Application Architecture. The diagram below illustrates the repo structure and domain mappings for each service.

## Repository Structure

The overall structure is detailed in the diagram below. It demonstrates how the shared UI repository (`waterstones-ui`) is integrated into each of the other services. Each application imports components from `waterstones-ui` to maintain consistency and maximize the reuse of design assets.

![Repository Structure](./assets/repo-structure.svg)

## Architecture Overview

The architecture is built around a shared UI component library and four core application services:

- **waterstones-ui**  
  *Purpose*: Contains reusable UI components and design assets.  
  *Note*: No associated domain.

- **waterstones-listing-web**  
  *Domain*: [waterstones.com](https://waterstones.com)  
  *Purpose*: Delivers the book browsing experience for general users.

- **waterstones-www-web**  
  *Domain*: [www.waterstones.com](https://www.waterstones.com)  
  *Purpose*: Serves as the main landing page, providing key information and navigation.

- **waterstones-customer-web**  
  *Domain*: [app.waterstones.com](https://app.waterstones.com)  
  *Purpose*: Manages customer functionalities such as account management and personalized services.

- **waterstones-auth-web**  
  *Domain*: [auth.waterstones.com](https://auth.waterstones.com)  
  *Purpose*: Handles authentication processes including sign in and sign up.

## Diagram Layout

- **Top**: `waterstones-ui`
- **Below (in one row)**:
  - `waterstones-listing-web`
  - `waterstones-www-web`
  - `waterstones-customer-web`
  - `waterstones-auth-web`

All four application repositories import components from **waterstones-ui** to ensure design consistency and shared functionality.

## Repo Descriptions

- **waterstones-ui**  
  Contains all shared UI components and design resources, ensuring a unified look and feel across all applications.

- **waterstones-listing-web**  
  Implements the book browsing interface with search and filter capabilities, leveraging the shared UI components.

- **waterstones-www-web**  
  Provides the primary entry point for users, offering navigation and essential content using a responsive design.

- **waterstones-customer-web**  
  Focuses on customer-specific interactions, such as account management and order tracking, using shared UI elements for a seamless experience.

- **waterstones-auth-web**  
  Manages authentication tasks with an emphasis on security and integration with the other services by reusing common UI components.

# Prometheus: Add README for task-template

## Project Overview

The Koii Task Template is a comprehensive development framework for creating decentralized tasks on the Koii Network. It provides developers with a structured, modular approach to building blockchain-based applications that can be executed across a distributed network of nodes.

### Core Purpose
This template enables developers to create scalable, decentralized tasks with built-in mechanisms for task execution, submission, auditing, and incentive distribution. It serves as a foundational toolkit for building blockchain applications that can run autonomously and securely across multiple nodes.

### Key Features
- **Modular Task Architecture**: Organized into distinct files for setup, core logic, submission, auditing, and reward distribution
- **Flexible Task Development**: Supports creating complex decentralized applications with customizable logic
- **Built-in Consensus Mechanism**: Implements a round-based task flow with automatic performance verification
- **Incentive Engineering**: Provides framework for defining reward and penalty mechanisms
- **Testable Infrastructure**: Includes commands for local testing, simulation, and production debugging
- **Typescript Support**: Leverages TypeScript for enhanced type safety and developer experience

### Benefits
- Simplifies blockchain task development with a comprehensive, well-structured template
- Reduces complexity of creating distributed computing applications
- Provides a standardized approach to decentralized task implementation
- Enables developers to focus on core application logic rather than infrastructure complexities

## Getting Started, Installation, and Setup

### Prerequisites

Before you begin, ensure you have the following:

- **Node.js** (version >=20.0.0, LTS Versions only)
- **Yarn** package manager
- *(Optional)* Docker Compose (for Docker-based tasks)

### Quick Start

1. Clone the repository:
   ```sh
   git clone https://github.com/koii-network/task-template.git
   cd task-template
   ```

2. Install dependencies:
   ```sh
   yarn install
   ```

### Development Workflow

#### Running Tests
To test your core task logic:
```sh
yarn test
```

#### Simulating Full Task Cycle
To simulate the entire task flow, including task performance, submission, and auditing:
```sh
yarn simulate
```

### Building for Production

1. Build the executable:
   ```sh
   yarn webpack
   ```

2. Create a `.env` file by copying the example:
   ```sh
   cp .env.developer.example .env
   ```

3. Run the production debugger:
   ```sh
   yarn prod-debug
   ```

### Deployment Preparation

1. Configure your task by editing `config-task.yml`
2. Deploy your task using the Create Task CLI:
   ```sh
   npx @_koii/create-task-cli@latest
   ```

### Development Tips

- Customize task logic in `src/task/1-task.ts`
- Explore additional task files for advanced configurations:
  - `0-setup.ts`: Initial setup steps
  - `2-submission.ts`: Proof submission
  - `3-audit.ts`: Work auditing
  - `4-distribution.ts`: Reward distribution
  - `5-routes.ts`: Custom routes

**Note:** Ensure you have a Koii wallet ready for deployment. You can create one using the [Desktop Node](https://koii.network/node) or [Koii CLI](https://docs.koii.network/develop/command-line-tool/koii-cli/install-cli).
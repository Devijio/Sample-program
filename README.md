
# DIMS_Automation

## Table of Contents

- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
- [Components](#components)
- [Usage](#usage)
- [Contribution](#contribution)
- [License](#license)

## Project Overview

IMS offers a comprehensive solution for managing and monitoring different aspects of infrastructure. The project structure is divided into various categories, each addressing specific requirements:

## Getting Started

To use the DIMS_AutomationIMS project, follow these steps:

1. Run the `initial/setup.sh` script to initialize the environment and set up essential components.
2. [Add any additional project-specific steps here]

## Components

### Initial Setup

The `initial/setup.sh` script performs the following tasks:

- Sets up directories for mountable volumes.
- Installs the `docker-compose.yaml` configuration.
- Starts the Docker database server.
- Collects admin email.
- Launches DIMS server (UI + Backend) and nginx containers.
- Creates 'admin' user in the database.
- Sends email to admin with encoded password.
- Generates academic calendar data.
- Sets up crontab entry for `scheduler.py`.

### Scheduler

The `scheduler/scheduler.py` script serves as the core scheduling system, utilizing methods from `common/common.py`.

### MDM (Mobile Device Management)

MDM providers include:

- Jamf: `mdm/jamf.py`
- Meraki: `mdm/meraki.py`
- Google: `mdm/google.py`
- Intune: `mdm/intune.py`

### Inventory

Inventory management modules include:

- TipWeb: `inventory/tipweb.py`
  1. Retrieves data from JAMF.
  2. Writes data to MDM table.
- IncidentIQ: `inventory/incidentiq.py`
  1. Retrieves data from JAMF.
  2. Writes data to MDM table.

[... continue for other sections ...]

## Usage

[Explain how to use each component]

## Contribution

Contributions are welcome! Follow these guidelines:

1. Fork the repository.
2. Create a new branch.
3. Commit changes.
4. Submit a pull request.

## License

[Specify the license information]


# wtg_flow
Workflow management for Offshore Wind Turbine Generator (WTG) structures.

## Introduction
`wtg_flow` provides a range of services to help complete and manager the design of offshore WTG structures. 
Many of the workflow components are also useful for the integrity management of existing offshore WTG structures.

The `wtg_flow` system is split into a number of components. Note that each of these components is managed within it's own repository:
- `wtg_environment` - to define and derive environmental conditions and design load cases (DLCs)
- `wtg_structure` - to define the sub-structures and output the models in a selection of generalized and proprietary (or user provided) formats
- `wtg_simulate` - to manage simulating the structures using distributed computing
- `wtg_interogate` - to visualize and interrogate simulation results
- `wtg_iterate` - wrapper around the other processes to optimize the structure based on the available criteria

Note that the software modules used by the aforementioned components have considerable overlap.

## Technology
`wtg_flow` uses web-based technology to provide the user with options to deploy `wtg_flow` locally or remotely.

### Graphical User Interface
- Python Dash/Plotly
- React.js to define unique components to be used within the Dash framework
- three.js to handle 3D visuals / user interaction

### Data storage
- HDF5 databases to store persistent numerical data
- PostgreSQL databases to store non-numerical data
- (SQLite databases to store non-numerical data for development purposes only)

### APIs
- Python FastAPI

### Deployment
- Docker
- Template docker containers provided to allow users to install their choice of solver software

### High Throughput Computing
- htcondor

### Solvers
- user's choice...

### Workflow Management
- Apache Airflow

### Hardware
- Local machines with Docker installed
- MS Azure (CycleCloud platform with htcondor scheduling)

## Notes
- Reverse proxy server to improve security and have single access point to communicate with multiple services?
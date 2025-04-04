# How to Update a Chart

1. Build the Helm package at the root path of the project:
   ```sh
   helm package <chart-name> # e.g., helm package ./charts/hybiot-chart -d .
   ```
   This command generates a `<chart-name>-<version>.tgz` file (e.g., hybiot-chart-1.0.0.tgz) at the root of your project directory.

2. Upload the package to your Helm repository on Azure:
   ```sh
   helm push <chart-name>-<version>.tgz <registry> # e.g., helm push hybiot-chart-1.0.0.tgz oci://bluestone.hybiot.io/charts
   ```
   Replace <registry-name> with the name of your Container Registry Helm repository (e.g., harbor). This command pushes the generated .tgz file to your Helm repository.

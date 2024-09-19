# steamcmd-docker-arm64-cpumhz
# Forked from https://github.com/TeriyakiGod/steamcmd-docker-arm64

This forked repository provides a Docker image for running SteamCMD on ARM64 architecture with a small tweak that sets the CPU clock speed variable, so it works, for example, on OCI Compute ARM64 machines. SteamCMD is a command-line utility that allows you to install and manage dedicated game servers via Steam.

## Prerequisites

- A machine or environment with ARM64 architecture support.
- Docker installed on your ARM64 system.

## Building the Docker Image

To build the Docker image, follow these steps:

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/3ehud/steamcmd-docker-arm64-cpumhz.git
   ```

2. Navigate to the repository's directory:

   ```bash
   cd steamcmd-docker-arm64-cpumhz
   ```

3. Build the Docker image using the provided `Dockerfile`:

   ```bash
   docker build -t steamcmd-arm64-cpumhz .
   ```

   This command will build the Docker image named "steamcmd-arm64-CPUMHZ."

## Running the SteamCMD Docker Container

Once you've built the Docker image, you can run the SteamCMD container using the following steps:

1. Run the SteamCMD container:

   ```bash
   docker run -it steamcmd-arm64-cpumhz
   ```

   This command starts an interactive session inside the container.
   When you start the container the steamcmd runs and updates immediately.

3. You can now use SteamCMD within the container to install and manage game servers. For example:

   ```bash
   Steam> login your_steam_username your_steam_password
   ```

   Replace `your_steam_username` and `your_steam_password` with your actual Steam credentials.

4. To exit the container when you're done, simply type `exit`.

5. If you need to make modifications to the container the root password is: `steamcmd`.

## Additional Information

- [SteamCMD Documentation](https://developer.valvesoftware.com/wiki/SteamCMD)
- [Docker Documentation](https://docs.docker.com/)

The Dockerfile has SteamCMD platform type set to Windows.
Used FEX version is FEX-2404, one of the newer versions changed something and the container won't build. 

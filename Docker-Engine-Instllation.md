# How To Install Docker on Ubuntu

Docker is a popular platform for developing, shipping, and running applications inside containers. Here's how you can install Docker on Ubuntu:

## Step 1: Update Your System

Before installing Docker, it's a good idea to update your system's package index:

```bash
sudo apt-get update
```

## Step 2:	Install Required Packages

Install necessary packages to allow apt to use repositories over HTTPS:

```bash
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
```

## Step 3:	Add Docker’s Official GPG Key

Add Docker's official GPG key to your system:

```bash
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
```

## Step 4:	Add Docker’s APT Repository

Set up the Docker repository by adding the stable repository:

```bash
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

## Step 5: Install Docker

Install Docker:

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

## Step 6:	Start and Enable Docker

Start the Docker service and ensure it runs at startup:

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

## Step 7:	Verify Docker Installation

Verify that Docker is installed correctly by running the hello-world image:

```bash
sudo docker run hello-world
```

You should see a message saying "Hello from Docker!" indicating that Docker is installed and working correctly.

## Optional Step: Manage Docker as a Non-Root User

If you want to run Docker commands without sudo, add your user to the Docker group:

```bash
sudo usermod -aG docker $USER
```

Then log out and log back in for the changes to take effect.
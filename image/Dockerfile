# Use the official Ubuntu base image
FROM ubuntu:latest

# Install Git and OpenSSH
RUN apt-get update && \
    apt-get install -y git openssh-client && \
    apt-get clean

# Install GitHub CLI (gh)
RUN apt-get update && \
    apt-get install -y git openssh-client python3 python3-pip && \
    apt-get clean


# Set up a non-root user (optional but recommended for security)
RUN useradd -ms /bin/bash gh-cli-image-user
USER gh-cli-image-user

CMD ["/bin/bash"]

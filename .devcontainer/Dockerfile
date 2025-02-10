# Use the hugomods/hugo:exts image for extended Hugo functionality
FROM hugomods/hugo:exts

# Create a symlink from /workspace to /src
RUN ln -s /workspace /src

# Set the working directory for Codespaces inside the container
WORKDIR /workspace

# Copy project files into the container
COPY . /workspace

# Add any packages that is necessary
#RUN apk add --no-cache git

# Expose the default Hugo server port
EXPOSE 1313

# Default command to run the Hugo server
CMD ["server", "--bind", "0.0.0.0"]

# Pre-installed packages and features in the hugomods/hugo Docker image:
# - Hugo Extended (supports SCSS/SASS and WebP image processing)
# - Node.js and npm (for frontend tooling like PostCSS and Autoprefixer)
# - Git (for version control and managing submodules)
# - OpenSSH Client (for deployment workflows)
# - Rsync (for syncing files between environments)
# - SASS/SCSS Libraries (e.g., libsass for SCSS/SASS compilation)
# - WebP Support (libwebp for WebP image encoding)
# - Build Tools (gcc, g++, musl-dev, build-base, libc6-compat)
# - Default Working Directory: /src
# - Default User: hugo (UID: 1000, GID: 1000)
# - Multi-Platform Support: linux/amd64, linux/arm64
# - Default Shell: ash (/bin/sh)

# Start with Node
FROM node:12.15.0

# Install Yarn using curl output to stdout - pipe to bash
RUN curl -o- -L https://yarnpkg.com/install.sh | bash

# Make yarn available to SH and compose
ENV PATH="/root/.yarn/bin:${PATH}"

# Add CRA and Storybook to your Dev Image
RUN yarn global add create-react-app && \  
    yarn global add getstorybook

# All operations run from this directory
WORKDIR /usr/src/app/  
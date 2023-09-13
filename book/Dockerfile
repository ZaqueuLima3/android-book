# Use an official Ruby image as a parent image
FROM ruby:latest

# Set the maintainer label
LABEL maintainer="zaqueulima1@gmail.com"

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy the current directory contents into the container
COPY . .

# Install Jekyll and Bundler
RUN gem install jekyll bundler jekyll-watch


# Install any needed packages specified in Gemfile
RUN bundle install

# Make port 4000 available to the world outside this container
EXPOSE 4000

# Define environment variable
ENV JEKYLL_ENV=production

# Run jekyll serve when the container launches
CMD ["jekyll", "serve", "--host", "0.0.0.0", "--watch", "--force_polling"]

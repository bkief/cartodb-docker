FROM ihme/cartodb-mapsapi:5.3.1-1.0.0

# Copy resources.
COPY config/*.js /Windshaft-cartodb/config/environments/

EXPOSE 80

# We configure the application using just the base config here. Additional configuration files can
# be merged with the base by supplying their filenames as the CMD.
ENTRYPOINT [ "docker-entrypoint.sh", "base.config.js" ]

# We use the development example config by default. Alternatives:
# - production.js.example
# - staging.js.example
# - test.js.example
# OR extend this image by COPYing a custom config file into /Windshaft-cartodb/config/environments/
# and passing its name as the CMD.
CMD [ "development.js.example" ]

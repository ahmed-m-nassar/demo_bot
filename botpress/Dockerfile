FROM botpress/server:v12_31_8

# Set working directory
WORKDIR /botpress

# Ensure the /botpress/lang directory exists and set ownership to botpress user
# RUN mkdir -p /botpress/lang && chown -R 999:999 /botpress/lang
# RUN mkdir -p /botpress/data && chown -R 999:999 /botpress/data

# Set default permissions for all files in the /botpress directory
#RUN su && chown -R botpress:botpress /botpress/data

#RUN chmod -R 777 /botpress

# Default command to run the Botpress server
CMD ["./bp"]

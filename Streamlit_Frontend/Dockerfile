# Base image
FROM python:3.10.8

# Create application directory
RUN mkdir -p /app/frontend

# Set the working directory
WORKDIR /app/frontend

# Copy the Streamlit frontend files to the container
COPY Streamlit_Frontend/ .

# Upgrade pip and install required packages
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

# Install Streamlit
RUN pip install streamlit
RUN ./setup.sh
# Expose the Streamlit port
EXPOSE 8501

# Command to run the Streamlit app
ENTRYPOINT ["streamlit", "run"]
CMD ["Hello.py"]

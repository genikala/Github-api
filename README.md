#!/bin/bash
# GitHub API URL
API_URL="https://api.github.com"

#GitHub username  and personal  access token
USERNAME=$username
TOKEN=$token

# Uaer and repositery information
REPO_USERNAME=$1
REPO_NAME=$2


# Function to make a GET request to the GitHub API
function github_api_get {
    local endpoint="$1"
    local url="${TOKEN}" "$url"
}


# Function to list users with read access to the repository 
function list_users_with-access {
    local endpoint="repos/${REPO_OWNER}/$REPO_NAME/collaborators"


    # Fetch the list of colloborators on repositery
    colloborators="$endpoint" | jq -r '.[] | select(.permissions.pull ==

    # Dispaly the list of cooloborators with read access
    if [[ -z '$colloborators" ]]; then
        echo "no users with read access found for ${REPO_OWNER}/${REPO_NAME}."
    else
        echo "users with read access to ${REPO_OWNER}/${REPO_NAME]:"
        echo "$colloborators"
    fi
  }

  # Main Script

  echo "Listing users with read access to ${REPO_OWNER}/${REPO_NAME}..."
  list_users_with-read_access  
    

# Hydra Password Cracking Lab

This repository provides a sandboxed environment to learn how to use Hydra for password cracking. It includes a Python script that sets up a simple HTTP Basic Auth server for testing purposes, along with instructions on how to use Hydra to crack the password.

## Prerequisites

- Python 3.8+
- Hydra (can be installed via package managers like `apt` for Ubuntu)

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/hydra-password-cracking-lab.git
   cd hydra-password-cracking-lab
   ```

2. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Start the HTTP Basic Auth server:
   ```bash
   python start_http_server.py
   ```

## Usage

1. Open a new terminal window.

2. Use Hydra to crack the password for the user `admin`:
   ```bash
   hydra -l admin -P wordlist.txt http-get://localhost:80/
   ```

3. Monitor the output to see Hydra attempting to guess the password.

## Files

- `start_http_server.py`: Starts a simple HTTP server with Basic Auth for testing.
- `wordlist.txt`: A small wordlist for testing purposes.
- `requirements.txt`: Lists Python dependencies.
- `LICENSE`: Contains the license information.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
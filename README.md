# **ReconRover**

![ReconRover](https://img.shields.io/github/license/kathuluman/reconrover?color=blue&style=for-the-badge) ![Version](https://img.shields.io/github/v/tag/kathuluman/reconrover?color=blue&style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white)
![Version](https://img.shields.io/badge/version-5.0.0-green?style=for-the-badge)


**ReconRover** is a comprehensive subdomain and vulnerability scanner designed to automate the process of discovering and assessing security vulnerabilities and enumerating applications across a domain(s). It integrates powerful tools like `subfinder`, `nuclei`, `httpx`, and `katana` to deliver an extensive security analysis.

## **Features**

- **Subdomain Enumeration**: Uses `subfinder` to discover subdomains for the target domain.
- **Vulnerability Scanning**: Employs `nuclei` to identify CVEs and vulnerabilities.
- **HTTP Probing**: Utilizes `httpx` to gather information about HTTP services and their configurations.
- **Link Discovery**: Leverages `katana` to find and catalog links, including `.js`, `.php`, and other interesting files.
- **Detailed Results**: Outputs results in a structured format for easy analysis.

## **Installation**

To get started with ReconRover, you’ll need to have Python 3.x installed, along with the required dependencies. You can set up the environment using `pip`:

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/yourusername/reconrover.git
   cd reconrover
   ```

2. **Install Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

3. **Install Required Tools**:
   
   ```bash
   go install -v github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest
   go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
   go install github.com/projectdiscovery/katana/cmd/katana@latest
   go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
   ```

## Usage

```bash
chmod +x reconrover
./reconrover -d target.com -w target.com -t 40
./reconrover -s subdomains.lst -w target.com -t 40
```

# Secure Password Manager & Generator (PMG Secure)
#### Video Demo: <URL HERE>
#### Description:

A comprehensive password management solution built with Python, focusing on security, usability, and modern cryptographic standards. PMG Secure provides enterprise-grade password management capabilities with an intuitive user interface.

## Core Features

### Password Generation System
- Highly customizable password length (8-32 characters)
- Three-tier complexity system:
  1. Simple (Memory-Friendly)
     - Dictionary-based word combinations
     - Automatic capitalization
     - Numerical suffixes (100-999)
     - Ideal for memorable passwords
  
  2. Moderate (Balanced)
     - Mixed character sets
     - Guaranteed uppercase and lowercase
     - Numbers and basic symbols (!@#$%)
     - Enforced character variety
  
  3. Complex (Maximum Security)
     - Full ASCII character set
     - Special symbols
     - Maximum entropy
     - Cryptographically secure randomization

### Advanced Security Architecture
- Multi-layer encryption system:
  - PBKDF2 key derivation with 100,000 iterations
  - Fernet symmetric encryption (AES-128 in CBC mode)
  - SHA-256 password hashing
  - Unique salt generation per user
  
- Secure Storage Implementation:
  - Encrypted database (SQLite3)
  - Protected key storage
  - Unix file permissions (0o700)
  - Database integrity verification
  - Automatic corruption detection

### Modern User Interface
- Built with CustomTkinter
- Dark mode optimized
- Organized tab structure:
  1. Generate Password
     - Real-time strength assessment
     - Length slider (8-32)
     - Complexity selector
     - One-click copying
  
  2. Store Login
     - Website categorization
     - Encrypted username storage
     - Secure password vault
  
  3. Search Login
     - Quick credential retrieval
     - Secure decryption
     - Clipboard integration
  
  4. Browse Login
     - Complete credential overview
     - Secure deletion options
     - Password visibility toggle
  
  5. Check Password
     - Comprehensive strength analysis
     - Security recommendations
     - Pattern detection

## Technical Specifications

### File Structure
~/.pmg_secure/ 
  ├── pmg_secure.db # Encrypted SQLite database 
  └── pmg_secure.key # Key storage file



### Security Measures
1. **Authentication**:
   - Secure session management
   - Brute force protection

2. **Data Protection**:
   - All sensitive data is encrypted before storage.
   - Passwords are hashed using SHA-256 for secure verification.

3. **Database Security**:
   - The database is encrypted and protected with strict file permissions.
   - Integrity checks are performed to ensure data consistency.

### Installation and Setup
1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Create and activate a Virtual Environment**:
  ```bash
  python -m venv venv
  source venv/bin/activate
  ```

3. **Install Dependencies**:
  ```bash
  pip install -r requirements.txt
  ```

4. **Run the Application**:
  ```bash
  python pmg_gui.py
  ```
  - This will open the app window and automatically set up the database.

## Usage
- Login/Register:
  - Use the login window to access or create your account.
- Password Management:
  - Use the tabs to generate, store, search, browse and manage your passwords securely.

## Contribution
Feel free to fork the repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
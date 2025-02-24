# Installation & Setup

### Installation & Setup

#### **System Requirements**

* **Operating System**: Developed on Windows
* **Python Version**: Developed and tested on 3.9, 3.11
* **Database**: OracleDB
* **Dependencies**: See `requirements.txt`

#### **Installation Steps**

1.  **Clone the Repository**

    ```
    git clone https://github.com/your-repo/aml-system.git
    cd aml-system
    ```
2.  **Create a Virtual Environment** (Recommended)

    ```
    conda create -n my_env python=Versions
    ```
3.  **Install Dependencies**

    ```
    conda activate my_env
    pip install -r requirements.txt
    ```
4. **Set Up Database Connection**
   * Ensure OracleDB is running.
   * Configure database credentials in `config/configuration.json`. (It should already be configured in the file.)
5.  **Run the System**

    ```
    python main.py
    ```

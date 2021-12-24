# signals-processing

## Set-up Instructions

1. Install [Python Version 3.7.9](https://www.python.org/downloads/release/python-379/)
for your operating system. Ensure that you have installed it correctly by running:

    ```bash
    # Show the current running version of python on your machine
    python --version
    ```

2. Create a [virtual environment](https://docs.python.org/3/library/venv.html)
in the root directory ``./signals-processing/venv`` by using the following
command:

    ```bash
    # Create a virtual environment (venv) in the venv directory
    python -m venv venv

    # Activate the virtual environment (Windows)
    ./venv/Scripts/activate.bat
    ```

1. Activate the virtual environment. In order to use a python venv, you have to
activate it in the terminal you are going to run further commands. There are multiple
ways depending on your choice:

    - In VSCode use the shortcut ``CTRL + SHIFT + P``, then Select Python interpreter
   and select the Python located in the local venv directory.
    - Using Admin Powershell [allow scripts](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.2) to be run by using:

       ```Powershell
       Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine
       ```

       Then run the [activation script](https://docs.python.org/3/library/venv.html):

       ```Powershell
       .\venv\Scripts\Activate.ps1
       ```

    If you succeded, test by opening a terminal where you should see the ``(venv)``
symbol prepended to each command.

1. Ensure that [pip](https://pypi.org/project/pip/) is installed and upgrade it:

    ```bash
    # Make sure it is installed. In case it is not, it will be installed.
    python -m ensurepip

    # Upgrade the pip version
    python -m pip install --upgrade pip
    ```

2. For each subproject you will find the [necessary dependencies](https://pip.pypa.io/en/stable/user_guide/) in the ``requirements.txt`` file. Install them using the following command:

    ```bash
    # Install the subproject dependencies in the venv
    pip install -r ./subproject/requirements.txt
    ```
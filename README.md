# Focus CLI

*ALL Website blocker extensions are trash, use this instead*.  
Use **only one website at a time**. No tab switching.  
Focus CLI is a command-line tool which helps you block distractions by locking your screen, preventing specific keys, and setting up timed focus and break intervals. 

## Features

- Pomodoro sessions with customizable focus and break times
- Focus protection that limits distractions during sessions, and prevents fidgeting with mouse
- Session stats tracking
- URL launcher for focus-related website. ONLY ONE.

## Installation

To install Focus CLI, follow these steps:

1. **Clone the repository:**

    ```bash
    git clone https://github.com/datavorous/focus_cli.git
    cd focus_cli
    ```

2. **Install dependencies:**

    Make sure you have [Poetry](https://python-poetry.org/) installed, then run:

    ```bash
    poetry install
    ```

3. **Activate the virtual environment:**

    ```bash
    poetry shell
    ```

## Usage

> [!NOTE]
> This was not intended for a retarded browser like Edge (which easily allows you to escape full screen mode with a right click, use Brave be happy.
> Or make a PR which prevents right mouse click, I ain't doing it for no reason.

```bash
focus
```

You'll be prompted to configure your Pomodoro session by setting the number of sessions, focus duration, and break duration. Focus protection will kick in, limiting distractions and guiding you through your work intervals.

> [!WARNING]
> The prebuilt binaries allows escaping, to prevent that, make the required changes in the ```focus_protection.py``` file and build it. Check out ```config.py``` aswell.

### Example

```bash
Sessions: 4
Focus (min): 25
Break (min): 5
Focus URL: https://example.com
Start? [y/n]: y
```

## Building an Executable

To build a standalone executable, follow these steps:

1. **Install PyInstaller:**

    ```bash
    poetry add pyinstaller
    ```

2. **Build the executable:**

    Run the following command to create a standalone executable:

    ```bash
    python build.py
    ```

3. **Find the executable:**

    The executable will be created in the `dist/` directory.
    Now put it in your env vars or whatever, just use `focus` anywhere on the cmd line.

## Contributing

Feel free to submit issues and pull requests for improvements!

## License

This project is licensed under the MIT License.
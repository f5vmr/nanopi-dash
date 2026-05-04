# SvxLink Configuration Dashboard

This is a Python3 Flask web application that provides a dashboard to view and edit the SvxLink configuration file (`svxlink.conf`).

## Features

- Node type selection (Simplex/Repeater) that enables the appropriate logic section.
- Displays all configuration sections and parameters in a web interface.
- Allows editing of parameters through a form.
- Saves changes back to the configuration file with automatic backups.
- Accessible at `hostname.local/install` (assuming hostname is set to 'svxlink').

## Installation

1. Ensure Python3 is installed.
2. Install dependencies:
   ```
   pip3 install -r requirements.txt
   ```

## Running the Application

To run the dashboard:

```
python3 app.py
```

This runs the Flask app on port 5002, accessible at `http://localhost:5002/`.

For production on the NanoPi (assuming hostname 'svxlink'), modify `app.py` to run on port 80 and use:

```
sudo python3 app.py
```

Then access at `svxlink.local/`.

## Usage

- Start by visiting the root URL to configure the node type (Simplex or Repeater).
- Then, the dashboard will guide you to `/setup` to view and edit the configuration parameters.
- Check/uncheck boxes to enable/disable parameters (adds/removes `#`).
- Click "Save Changes" to update the file (a backup `svxlink.conf.bak` is created automatically).

## Usage

- Navigate to `svxlink.local/setup` in your browser.
- View and edit the configuration parameters.
- Click "Save Changes" to update the file.

## Future Enhancements

- Add validation for parameter values.
- Include descriptions or comments from the config file.
- Add functionality to restart SvxLink service after changes.
- Improve the UI styling.
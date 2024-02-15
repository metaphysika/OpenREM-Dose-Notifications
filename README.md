# OpenREM-Dose-Notifications

## Overview
The OpenREM Dose Alerts system is a critical addition to the OpenREM suite, designed to automatically send email alerts for CT, fluoroscopy, and radiography exams that exceed predefined dose thresholds. This functionality helps medical physicists and radiology departments monitor and investigate high-dose incidents promptly, ensuring patient safety and compliance with regulatory standards. OpenREM comes configured with the ability to send fluoroscopy alerts. This script aims to expand that to CT.

## Features
- Automated dose alerts for CT exams.
- Customizable dose thresholds for different imaging protocols.
- Integration with OpenREM's RDSR processing for real-time alerting.
- Support for both text and HTML email templates for comprehensive and readable alerts.
- Test email functionality to verify configuration and email delivery.

## Installation
Before installing the OpenREM Dose Alerts system, ensure you have an operational OpenREM environment.

1. Clone this repository or download the `send_high_dose_alert_emails.py` script to your OpenREM server.
2. Place the script in a directory accessible by the OpenREM application, typically within the OpenREM project folder.

## Configuration
1. **Email Settings**: Configure your OpenREM project's email settings in `openremproject/settings.py` to enable email sending capabilities. This includes setting up the SMTP host, port, sender email, and authentication details.
2. **Dose Thresholds**: Customize dose thresholds for alerts by editing the `HighDoseMetricAlertSettings` in the OpenREM database according to your requirements.
3. **Templates**: Modify the text and HTML email templates located in `remapp/templates/remapp/` to tailor the alert messages. Ensure the templates are named correctly and accessible to the script.

## Usage
The `send_high_dose_alert_emails.py` script is triggered by OpenREM's RDSR processing module (`rdsr.py`) when an incoming exam exceeds the specified dose thresholds. To manually test or run the script, follow these steps:

1. Navigate to the directory containing the script.
2. Execute the script with Python, specifying any required arguments:

python send_high_dose_alert_emails.py


## Testing
To send a test email, use the test functionality within the script, providing a test user email address. This helps validate the email configuration and template rendering before deploying the alert system in a production environment.

## Contributing
Contributions to enhance the OpenREM Dose Alerts system, such as improvements to the email templates, dose calculation logic, or configuration options, are welcome. Please submit pull requests or raise issues on the GitHub repository.

## License
This project inherits the license from the OpenREM project, which is distributed under the GNU General Public License v3.0. See the LICENSE file for more details.

## Acknowledgments
- OpenREM for the foundational radiology examination monitoring tools.
- Contributors who have provided valuable feedback and code contributions to this project.


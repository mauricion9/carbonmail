# carbonmail

A Python library for carbon-aware email management and sending.

## Overview

carbonmail is a lightweight Python library designed to help reduce the carbon footprint of email communications. It provides tools for optimizing email sending times, managing attachments efficiently, and monitoring the environmental impact of email operations.

## Features

- **Carbon-aware scheduling**: Optimize email sending times based on grid carbon intensity
- **Efficient attachment handling**: Smart compression and optimization of email attachments
- **Carbon footprint tracking**: Monitor and report on the environmental impact of email operations
- **Multiple email provider support**: Works with SMTP, SendGrid, Amazon SES, and other popular email services
- **Easy integration**: Simple API that works with existing email workflows

## Installation

```bash
pip install carbonmail
```

## Quick Start

```python
from carbonmail import CarbonMailClient

# Initialize the client
client = CarbonMailClient(
    smtp_host='smtp.example.com',
    smtp_port=587,
    username='your_username',
    password='your_password'
)

# Send a carbon-optimized email
client.send_email(
    to='recipient@example.com',
    subject='Hello from carbonmail',
    body='This email was sent with carbon awareness!',
    optimize_timing=True
)

# Check carbon footprint
stats = client.get_carbon_stats()
print(f"Total CO2 saved: {stats['co2_saved']} grams")
```

## Configuration

carbonmail can be configured using environment variables or a configuration file:

```python
# Using environment variables
export CARBONMAIL_SMTP_HOST=smtp.example.com
export CARBONMAIL_SMTP_PORT=587
export CARBONMAIL_USERNAME=your_username
export CARBONMAIL_PASSWORD=your_password

# Or using a config file
client = CarbonMailClient.from_config('config.json')
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For issues, questions, or contributions, please open an issue on the GitHub repository.

## Acknowledgments

- Carbon intensity data provided by various grid carbon intensity APIs
- Inspired by the need for sustainable software practices
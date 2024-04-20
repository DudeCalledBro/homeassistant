# HomeAssistant

This repository contains my ansible deployment for Home Assistant. I am using Home Assistant with Docker, because it's the most flexible and easiest solution for me.

## Prerequisites

- Ensure you have Ansible installed (e.g. `pip3 install ansible`)
- Ensure Docker is installed on the Home Assistant server (you may want to checkout my [ansible-docker-role](https://github.com/DudeCalledBro/ansible-role-docker))

## Installation

1. Copy the `example.inventory.yml` file to `inventory.yml` and setup as you need. Ensure you also check the role's defaults.

2. Run the Ansible playbook to deploy Home Assistant

    ```bash
    ansible-playbook play-homeassistant.yml
    ```

> You may have to enter a password to SSH into the target system, so you need to add `-k` after the `ansible-playbook` command.

## Setup Home Assistant

1. Enther the Home Assistant web gui (e.g. `https://homeassistant.local:8123`)

2. Create a new smart home by pressing `create my smart home`

3. In the third step it's required to create a new user

    - Name: `Niclas Spreng`
    - Username: `duecalledbro`
    - Password: `<some_password>` (and confirmation)

4. Set the Home location (e.g. `Munich`)

5. Now it's getting interesting - you may want to enable some analytics.

    - Disable: Basic analytics
    - Disable: Usage
    - Disable: Statistical data
    - Disable: Diagnostics

6. Finish setup!

## License

Copyright © 2024 Niclas Spreng

Licensed under the [MIT license](LICENSE).

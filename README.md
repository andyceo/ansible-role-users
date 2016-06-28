# Ansible Role: users

Add users, create custom configurations.

## Requirements

Ubuntu 16.04

## Variables

This role contain one variable `users`. Thia ia dictionary of form:

    users:
      username:
        
        # Generate or not SSH key (Default: no)
        generate_ssh_key: yes
        
        # Add user to passwordless sudo (Default: no)
        sudoers_passwordless: yes

        # Create home directory (Default: yes)
        createhome: yes
        
        # State of user (add or remove) (Default: present)
        state: present
        
        # Password (in crypted form). To crypt password "guest123" for username "guest", use:
        # python -c 'import crypt; print crypt.crypt("guest123", "guest")
        # the above code will produce gu2KmqcJp0Yyo
        password: gu2KmqcJp0Yyo
        
        # Should password be updated on every ansible run (Default: always)
        update_password: always

        # List of groups user should belongs to (sudo group for administration) (Default: username)
        groups: sudo
        
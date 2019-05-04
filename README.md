[Deprecated. Use confluence-docker instead](https://github.com/calvinbui/ansible-confluence-docker)

# Ansible Confluence

Installs Confluence following the official documentation.

Uses the following folder structure:

```
confluence/
  data/
  running/ -> confluence/versions/atlassian-confluence-6.12.2
  versions/
    atlassian-confluence-6.11.0
    atlassian-confluence-6.12.2
```

##  Requirements

- Java
- Postgres

## Role Variables

`confluence_version`: Version to download and run

`confluence_user`: User to run confluence as, will be created

`confluence_download_link`: URL to download Confluence

`confluence_running_dir`:  Directory of running Confluence instance

`confluence_downloads_dir`: Directory to download Confluence tars to

`confluence_versions_dir`: Directory to store versions of Confluence when unpacked

`confluence_data_dir`: Directory of Confluence data

## Dependencies

N/A

## Example Playbook

```yaml
- hosts: servers
  become: true
  roles:
    - role: calvinbui.ansible_confluence
```

## License

GPLv3

## Author Information

http://calvin.me


# Tracker-Client File Sharing System Commands

This document provides the essential commands for using the Tracker-Client-based file sharing system.

## Tracker Commands

- **Run Tracker**:
  ```bash
  ./tracker tracker_info.txt <tracker_no>
  ```
  - `tracker_info.txt`: File containing IP and port details of all trackers.
  - `<tracker_no>`: Tracker number identifier.

- **Close Tracker**:
  ```bash
  quit
  ```

## Client Commands

- **Run Client**:
  ```bash
  ./client <IP>:<PORT> tracker_info.txt
  ```
  - `<IP>:<PORT>`: IP and port of the tracker.
  - `tracker_info.txt`: File containing details of all trackers.

### User Management

- **Create User Account**:
  ```bash
  create_user <user_id> <passwd>
  ```

- **Login**:
  ```bash
  login <user_id> <passwd>
  ```

- **Logout**:
  ```bash
  logout
  ```

### Group Management

- **Create Group**:
  ```bash
  create_group <group_id>
  ```

- **Join Group**:
  ```bash
  join_group <group_id>
  ```

- **Leave Group**:
  ```bash
  leave_group <group_id>
  ```

- **List Pending Join Requests**:
  ```bash
  list_requests <group_id>
  ```

- **Accept Group Joining Request**:
  ```bash
  accept_request <group_id> <user_id>
  ```

- **List All Groups in the Network**:
  ```bash
  list_groups
  ```

### File Sharing

- **List All Shareable Files in a Group**:
  ```bash
  list_files <group_id>
  ```

- **Upload File**:
  ```bash
  upload_file <file_path> <group_id>
  ```

- **Download File**:
  ```bash
  download_file <group_id> <file_name> <destination_path>
  ```

- **Stop Sharing a File**:
  ```bash
  stop_share <group_id> <file_name>
  ```

### Additional Commands

- **Show Downloads**:
  ```bash
  show_downloads
  ```
  - Output format:
    - `[D] [grp_id] filename` (Downloading)
    - `[C] [grp_id] filename` (Complete)

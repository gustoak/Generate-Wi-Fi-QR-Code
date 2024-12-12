# Generate Wi-Fi QR Codes Directly on Your Laptop

You can use the **WiFi QR Code Generator** tool to create QR Codes that, when scanned, automatically connect a device to the specified Wi-Fi network.

---

## Installation

### 1. Install Python
Ensure Python is installed on your system. You can download it from [python.org](https://www.python.org/).

### 2. Install the `wifi-qrcode-generator` Library
In the terminal, run the following command to install the required library:

```bash
pip install wifi-qrcode-generator
```

---

## Usage

Once installed, you can generate a QR Code for your Wi-Fi network using the following command:

```bash
python -m wifi_qrcode_generator -S  NETWORK_NAME -a NETWORK_PASSWORD -p SENHA_DA_REDE -o NETWORK_PASSWORD
```

> **Important**: Do **not** include quotes (`"`) around the parameter values. The script will not process them correctly if quotes are used.

---

## Parameters

- `-S`: Specify the **network name** (SSID).
- `-a`: Specify the **security type** (e.g., WPA, WEP, or `nopass` for networks without a password).
- `-p`: Provide the **network password**.
- `-o`: Define the **output file path and name** for the QR Code image.

---

## Examples

### Example 1: Save in the Current Directory

To generate a QR Code for a Wi-Fi network named `MyNetwork` using WPA security and password `mypassword123`, and save it as `wifi_qrcode.png` in the current directory:

```bash
python -m wifi_qrcode_generator -S MyNetwork -a WPA -p mypassword123 -o wifi_qrcode.png
```

### Example 2: Save in a Specific Directory

To save the QR Code in a specific directory:

```bash
python -m wifi_qrcode_generator -S MyNetwork -a WPA -p mypassword123 -o /path/to/directory/qrcode_wifi.png
```

> **Note**: Ensure the directory exists and that you have write permissions.

### Example 3: Generate for an Open Network (No Password)

For an open network named `GuestNetwork` without a password:

```bash
python -m wifi_qrcode_generator -S GuestNetwork -a nopass -o guest_wifi_qrcode.png
```

---

## Key Points

1. Use the `-S` parameter for the **network name** (SSID).
2. Use the `-a` parameter for the **security type** (`WPA`, `WEP`, or `nopass`).
3. Use the `-p` parameter for the **network password** (leave it out if using `nopass`).
4. Use the `-o` parameter to define the **output file path and name**.
5. **Do not include quotes** (`"`) around parameter values.

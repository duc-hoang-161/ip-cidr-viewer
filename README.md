# IP CIDR Viewer

A simple web-based application to check if IP addresses match a given CIDR range.

## Features

- ✅ Input multiple IP addresses in comma-separated format
- ✅ Check if each IP belongs to a specified CIDR range
- ✅ Visual indication of matches and non-matches
- ✅ Summary statistics showing total IPs, matches, and non-matches
- ✅ Clean and responsive UI

## Usage

### Option 1: Open Directly in Browser

Simply open `index.html` in your web browser. No server required!

```bash
# On Linux/Mac
open index.html

# On Windows
start index.html
```

### Option 2: Using a Local Server

If you prefer to use a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (if you have http-server installed)
npx http-server

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000` in your browser.

## How to Use

1. **Enter IP Addresses**: Input one or more IP addresses separated by commas in the first field
   - Example: `192.168.1.1, 192.168.1.5, 10.0.0.1`

2. **Enter CIDR Range**: Input the CIDR notation in the second field
   - Example: `192.168.1.0/24`

3. **Click "Check IPs"**: The application will display which IPs match the CIDR range

## Examples

### Example 1: Local Network Check
- **IPs**: `192.168.1.1, 192.168.1.100, 192.168.2.1`
- **CIDR**: `192.168.1.0/24`
- **Result**: First two IPs match, third one doesn't

### Example 2: Class A Network
- **IPs**: `10.0.0.1, 10.255.255.254, 11.0.0.1`
- **CIDR**: `10.0.0.0/8`
- **Result**: First two IPs match, third one doesn't

### Example 3: Single Host
- **IPs**: `8.8.8.8, 8.8.4.4`
- **CIDR**: `8.8.8.8/32`
- **Result**: Only the first IP matches

## Technical Details

The application uses JavaScript to:
- Parse and validate IP addresses
- Parse and validate CIDR notation
- Convert IP addresses to 32-bit integers for comparison
- Apply subnet masks to determine if an IP belongs to a CIDR range

## Browser Support

Works in all modern browsers:
- Chrome
- Firefox
- Safari
- Edge

## License

MIT
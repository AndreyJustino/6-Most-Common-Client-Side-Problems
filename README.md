# Introduction

This documentation presents six common errors that affect client-side browsing, explaining their causes and offering practical solutions. Understanding these issues, such as DNS failures and connection refusals, is essential to improving efficiency in resolving connectivity issues and ensuring smoother browsing.

## 1. DNS_PROBE_FINISHED_NXDOMAIN

This error is common and indicates that the browser cannot resolve the DNS (Domain Name System) for an IP address, which is necessary to access websites.

### Possible causes:
- Incorrect DNS configuration or DNS server not responding.
- Non-existent or not yet propagated domain name.
- Internet connection issues.
- Firewall or antivirus software blocking the connection.
- Incorrectly configured local hosts file.

### How to fix:
1. **Check the URL**: Make sure the website address is entered correctly.
2. **Clear the DNS cache**:
   - Windows: `ipconfig /flushdns`
   - macOS: `sudo killall -HUP mDNSResponder`
   - Linux: `sudo systemd-resolve --flush-caches`
3. **Restart the modem and router**: Turn them off, wait 30 seconds, and turn them back on.
4. **Change the DNS server**: Set up alternative DNS servers such as:
   - Google DNS: `8.8.8.8 / 8.8.4.4`
   - OpenDNS: `208.67.222.222 / 208.67.220.220`
   - Cloudflare DNS: `1.1.1.1 / 1.0.0.1`
   - Windows setup: In network connection properties, enter the new DNS addresses under "Internet Protocol Version 4 (TCP/IPv4)".
   - macOS setup: In network preferences, enter the new addresses under the "DNS" tab.
   - Android and iOS setup: Change the IP settings to "Static" or "Manual" and enter the DNS addresses.
5. **Disable VPN and Proxy**: Temporarily disable VPN or Proxy to check if they are interfering.
6. **Update network drivers**: Make sure they are up to date.
7. **Test on another device or browser**: To determine if the issue is specific to one device or browser.
8. **Check firewall and antivirus**: Temporarily disable them to see if they are blocking the connection.
9. **Contact your internet provider**: If the problem persists, contact your provider.

## 2. ERR_CONNECTION_TIMED_OUT

This error occurs when the browser cannot establish a connection with the server within a timeout period.

### How to fix:
- Check your internet connection and restart the router.
- Clear the browser cache and cookies.
- Temporarily disable the firewall and antivirus.
- Try accessing the website on another browser or device.
- Check proxy or VPN settings.
- Consult the website administrator to check for server issues.

## 3. ERR_CONNECTION_REFUSED

This error indicates that the connection to the server was refused, usually when the server is down or there are firewall blocks.

### How to fix:
- Check if the site is offline using tools like “Down For Everyone Or Just Me.”
- Restart the modem and router.
- Clear the browser cache and cookies.
- Temporarily disable the firewall and antivirus.
- Check proxy or VPN settings.
- Try accessing the site on another browser or device.
- Consult the website administrator.

## 4. ERR_NAME_NOT_RESOLVED

This error means that the browser could not find the IP address corresponding to the domain name.

### How to fix:
- Check if the website address is correct.
- Clear the DNS cache with `ipconfig /flushdns` (Windows) or `sudo killall -HUP mDNSResponder` (macOS).
- Change your DNS server to Google DNS or OpenDNS.
- Restart the modem and router.
- Try accessing the site on another browser or device.

## 5. ERR_SSL_PROTOCOL_ERROR

This error occurs when there is a problem with the SSL protocol, used for secure (https) connections.

### How to fix:
- Check the date and time on the device.
- Clear the browser cache and cookies.
- Temporarily disable antivirus or firewall.
- Update the browser to the latest version.
- Check SSL settings in the browser.
- Consult the website administrator about the SSL certificate.

## 6. ERR_NETWORK_CHANGED

Indicates that the network was changed during page loading, such as when switching Wi-Fi networks.

### How to fix:
- Check the network connection and reconnect if necessary.
- Restart the modem and router.
- Temporarily disable the firewall and antivirus.
- Clear the browser cache and cookies.
- Update the browser to the latest version.

# Conclusion

The errors presented in this paper are common in the daily lives of users and programmers, affecting web browsing and communication between clients and servers. Understanding their causes and solutions is essential to maintaining an efficient and secure online experience. With appropriate diagnostic and correction practices, such as checking DNS, updating drivers, and adjusting network settings, it is possible to quickly resolve these problems, avoiding interruptions and improving the quality of internet access. Thus, knowledge of these errors and their resolutions becomes a valuable tool for everyone involved in the development and maintenance of web systems.

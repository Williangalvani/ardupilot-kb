

```
import routeros_api

def get_voltage(username, password, host):
    client = routeros_api.RouterOsApiPool(host, username=username, password=password, plaintext_login=True)
    api = client.get_api()

    try:
        # Adjust the path according to where voltage information is stored in your RouterOS
        voltage_info = api.get_resource('/system/health').get()
        for info in voltage_info:
            if 'voltage' in info:
                return info['voltage']
        return "Voltage information not found"
    except Exception as e:
        return f"An error occurred: {e}"
    finally:
        client.disconnect()

# Replace with your RouterOS credentials and IP
username = 'admin'
password = ''
host = '192.168.2.3'

voltage = get_voltage(username, password, host)
print(f"RouterOS Voltage: {voltage}")
```

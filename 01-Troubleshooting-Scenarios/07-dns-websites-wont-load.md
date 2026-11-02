# Scenario 7: Websites won't load, but the network looks fine

Level: Harder
Note: Practice scenario. The details are fictional.

## Problem
A user says "the internet is down". Websites show an error, but the Wi-Fi icon shows connected.

## Symptoms
- The browser shows "server IP address could not be found" or "DNS_PROBE_FINISHED_NO_INTERNET"
- Other devices on the same Wi-Fi work normally
- Some apps that were already open (like Teams) still work

## Diagnostic steps
1. Check the laptop has a normal IP address. Run `ipconfig`. The address is 192.168.x.x, so it is not the 169.254 problem.
2. Test the connection without DNS. Run `ping 8.8.8.8`. It works, so the internet connection itself is fine.
3. Test with a name. Run `ping google.com`. It fails. The connection works, but names are not being turned into addresses. This points to DNS.
4. Check which DNS server the laptop uses. Run `ipconfig /all` and look at "DNS Servers". It shows an old address (192.168.1.5) that no longer exists.
5. Confirm it is DNS. Run `nslookup google.com`. It times out. Then run `nslookup google.com 8.8.8.8`. It works. The laptop's DNS setting is the problem.

## Root cause
The laptop had a manually typed DNS server from an old office setup. That server was switched off, so every name lookup failed.

## Solution
1. Open the network adapter settings and change DNS to "Obtain automatically"
2. Run `ipconfig /flushdns` to clear old lookups
3. Test again with `nslookup google.com` and open a website
4. Ask the user to confirm everything works

## Prevention
- Avoid typing DNS servers by hand. Let DHCP give out the correct ones.
- Update the DHCP settings when a DNS server is retired.
- Keep a short note of which DNS servers the network should use.

## What I learned
Pinging an IP address and pinging a name tells you whether the problem is the connection or DNS.

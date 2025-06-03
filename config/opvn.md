dev tun
persist-tun
persist-key
data-ciphers AES-128-GCM:AES-256-CBC
data-ciphers-fallback AES-256-CBC
auth SHA256
tls-client
client
resolv-retry infinite
remote [insert ip] tcp
nobind
verify-x509-name "OpenVPN-Server" name
auth-user-pass
remote-cert-tls server

<ca>
-----BEGIN CERTIFICATE-----
MIIDMzCCAhugAwI...
-----END CERTIFICATE-----
</ca>
  
<cert>
-----BEGIN CERTIFICATE-----
MIIDfTCC...
-----END CERTIFICATE-----
</cert>
  
<key>
-----BEGIN PRIVATE KEY-----
MIIEvAI......
-----END PRIVATE KEY-----
</key>
key-direction 1


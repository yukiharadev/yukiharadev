[General]
bypass-system = true
skip-proxy = 192.168.0.0/16,10.0.0.0/8,172.16.0.0/12,localhost,*.local,captive.apple.com,whoer.net
tun-excluded-routes = 10.0.0.0/8, 100.64.0.0/10, 127.0.0.0/8, 169.254.0.0/16, 172.16.0.0/12, 192.0.0.0/24, 192.0.2.0/24, 192.88.99.0/24, 192.168.0.0/16, 198.51.100.0/24, 203.0.113.0/24, 224.0.0.0/4, 255.255.255.255/32, 239.255.255.250/32
dns-server = system
fallback-dns-server = system
ipv6 = false
prefer-ipv6 = false
dns-direct-system = false
icmp-auto-reply = true
always-reject-url-rewrite = false
private-ip-answer = true
# direct domain fail to resolve use proxy rule
dns-direct-fallback-proxy = true
# The fallback behavior when UDP traffic matches a policy that doesn't support the UDP relay. Possible values: DIRECT, REJECT.
udp-policy-not-supported-behaviour = REJECT

[Rule]
DOMAIN-KEYWORD,whatsapp,PROXY
DOMAIN-SUFFIX,g.whatsapp.net,PROXY
DOMAIN,edge-mqtt.facebook.com,PROXY
DOMAIN-SUFFIX,i.instagram.com,PROXY
DOMAIN-KEYWORD,threads,PROXY
DOMAIN-KEYWORD,whatapp,PROXY
DOMAIN-SUFFIX,meta,PROXY
DOMAIN-SUFFIX,fb,PROXY
DOMAIN-KEYWORD,instagram,PROXY
DOMAIN-KEYWORD,facebook,PROXY
DOMAIN-KEYWORD,fbcdn,PROXY
# Block HTTP3/QUIC
# AND,((PROTOCOL,UDP),(DEST-PORT,443)),REJECT-NO-DROP
# Baidu/iqiyi
# Telegram
# DNS Leak
# LAN
# China
# Final

[Host]
localhost = 127.0.0.1

[URL Rewrite]
^https?://(www.)?g.cn https://www.google.com 302
^https?://(www.)?google.cn https://www.google.com 302

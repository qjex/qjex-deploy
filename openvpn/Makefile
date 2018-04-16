build:
	docker build -t qjex/openvpn .
run:
	-docker rm -f openvpn
	docker run -d --name openvpn -v /srv/openvpn:/etc/openvpn -p 0.0.0.0:1194:1194/tcp --cap-add=NET_ADMIN qjex/openvpn
add-client:
	docker run -v /srv/openvpn:/etc/openvpn --rm -it qjex/openvpn easyrsa build-client-full $(CLIENTNAME) nopass
get-client:
	docker run -v /srv/openvpn:/etc/openvpn --rm qjex/openvpn ovpn_getclient $(CLIENTNAME)
init:
	docker run -v /srv/openvpn:/etc/openvpn --rm qjex/openvpn ovpn_genconfig -u udp://vpn.qjex.xyz
	docker run -v /srv/openvpn:/etc/openvpn --rm -it qjex/openvpn ovpn_initpki

.PHONY: build run init add-client get-client

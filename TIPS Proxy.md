TIPS -- Configuracion Forward Proxy Interno SA

# PROXY
http://lan.prx.aap.aysa.ad:3128 (all)
NO PROXY=localhost,127.0.0.1,10.0.0.0/8,172.16.0.0/12,192.168.0.0/16,.aysa.ad

# Environment
export HTTP_PROXY=http://lan.prx.aap.aysa.ad:3128 
export HTTPS_PROXY=http://lan.prx.aap.aysa.ad:3128 
export NO_PROXY=localhost,127.0.0.1,10.0.0.0/8,172.16.0.0/12,192.168.0.0/16,.aysa.ad

export http_proxy=http://lan.prx.aap.aysa.ad:3128 
export https_proxy=http://lan.prx.aap.aysa.ad:3128 
export no_proxy=localhost,127.0.0.1,10.0.0.0/8,172.16.0.0/12,192.168.0.0/16,.aysa.ad

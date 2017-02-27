# note


diego windows: https://docs.pivotal.io/pivotalcf/1-8/windows/understand-windows.html#network-isolation
               https://docs.pivotal.io/pivotalcf/1-9/opsguide/deploying-diego.html




 wget  -c -O "cf-1.8.30-build.2.pivotal" --post-data="" --header="Authorization: Token 7jNFeXF66TGmy46Cb5RB"  https://network.pivotal.io/api/v2/products/elastic-runtime/releases/4352/product_files/14225/download
--2017-02-24 15:01:02--  https://network.pivotal.io/api/v2/products/elastic-runtime/releases/4352/product_files/14225/download




Set-Service RepService -startuptype "Disabled"

Invoke-WebRequest -Uri http://localhost:1800/evacuate -Method Post

while ($true) {
    try {
        Get-WebRequest "http://localhost:1800/ping"
    } catch {
        [system.exception]
        break;
    }
}

Set-Service RepService -startuptype "Automatic"

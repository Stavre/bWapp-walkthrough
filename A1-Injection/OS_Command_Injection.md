### Low

Very simple command injection: www.nsa.gov;id

### Medium

Simple command injection: www.nsa.gov|id

### High

So far I found common injections (|,||,&,&&,$(), etc) do not work. By the output given it appears the server uses nslookup. The frontend accepts multiple parameters. I assume  the backend uses nslookup . escapeshellcmd(). Due to the php version used \0 inside a string terminates that string, so escapeshellcmd(hello\0world) is actually escapeshellcmd(hello).

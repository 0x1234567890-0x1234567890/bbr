# bbr
A command line application to taketemplate information and process it over the command line. Useful for piping reporting from one application to another (such as an automatic submission tool).

# Arguments
| Argument | Description                      |
|----------|----------------------------------|
| -h       | Display help message and exit   |
| -r       | Path to template file to use    |
| -t       | Variable to replace \_target\_ with and to use for `dig` and `whois` commands. |
| -u       | Username to replace \_user\_ with |
| -o       | Output file name. (optional)       |
| -p | Variable to replace \_program\_ (optional) |
| -re | Variable to replace \_researcher\_ (optional) |
| -u | Variable to replace \_username\_ (optional) |

BBR will then process the text file, and make the following replacements (not all fields may be present, some will be present more than once):

| Argument      | Description                                               |
|---------------|-----------------------------------------------------------|
| \_target\_      | Replace with the value of the -t argument                |
| \_username\_    | Replace with the value of the -u argument                |
| \_program\_      | Replace with the value of the -p argument                |
| \_researcher\_ | Replace with the value of the -re argument |
| \_username\_ | Replace with the value of the -u argument |
| \_sha\_         | Replace with the SHA256 encoded value of the -u argument |
| \_nameservers\_ | Replace with the output of "dig NS @8.8.8.8 _target_"     |
| \_dig\_         | Replace with the value of "dig @8.8.8.8 _target_"         |
| \_whois\_       | Replace with the whois output of the target parameter    |
| \_wayback\_ | Replace with an automatic wayback link of the -t argument |
| \_sha\_ | Replace with the SHA256 value of the username parameter |
| \_dig-txt\_ | Replace with the value of DNS TXT records |
| \_curl\_ | Replace with the request response of the -t argument |
| \_joke\_ | Replace with a joke |
| \_punchline\_ | Replace with the punchline for said joke |

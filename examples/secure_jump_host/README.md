# Example `secure_jump_host`

## Usage

* Build Docker image
```shell
$> docker build . -t secure_jump_host:latest
```
* Start a container and provide an inventory and playbook
```shell
$> docker run -v $PWD:/deployment secure_jump_host:latest -i /deployment/inventory.ini /deployment/playbook.yml
```
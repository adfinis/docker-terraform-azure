# Azure CLI and Terraform in an Alpine Container

Container image based on `hasicorp/terraform` that contains the Azure CLI as
installed with pip.

## Usage

See the [hashicorp image](https://hub.docker.com/r/hashicorp/terraform/) for
details on using the terraform parts of this image.

```bash
docker run \
  --rm \
  -v $(pwd):/app/ \
  -w /app/ \
  -e ARM_SUBSCRIPTION_ID \
  -e ARM_TENANT_ID \
  -e ARM_CLIENT_ID \
  -e ARM_CLIENT_SECRET \
  adfinissygroup/terraform-azure
```

You'll have to provide the `ARM_*` variables in the above example to allow
Terraform to access your Azure subscription using a service principal.

## License

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.

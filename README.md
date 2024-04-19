# Keycloak Admin Client in CommonJS

This lib exports the [@keycloak/keycloak-admin-client](https://www.npmjs.com/package/@keycloak/keycloak-admin-client)
The idea is export as CommonJS the current type modules of keycloak-admin-client

An original idea from [Manuelbaun](https://github.com/Manuelbaun) in https://github.com/keycloak/keycloak-nodejs-admin-client/issues/523

the package version must match the current keycloak version exported

## Install

```shell
npm i @cognativ-inc/keycloak-admin-client
```

## Usage

```ts
import { KeycloakAdminClient } from '@cognativ-inc/keycloak-admin-client';

@Injectable()
export class KeycloakAdminService {
    private readonly kcAdmin: KeycloakAdminClient;

    constructor(logger: LoggingService) {
        this.log = logger.getLogger("KeycloakAdminService");
        this.kcAdmin = new KeycloakAdminClient();
    }
}
```
# doctrine-type-testcases

| Branch    | PHP                                         | Code Coverage                                        |
|-----------|---------------------------------------------|------------------------------------------------------|
| `master`  | [![PHP][build-status-master-php]][actions]  | [![Code Coverage][coverage-status-master]][codecov]  |

## Usage

### Installation

```bash
composer require datana-gmbh/doctrine-type-testcases
```



### Setup
```yaml
# config/packages/doctrine.yaml

doctrine:
    dbal:
        types:
            # We want to store DateTime objects with milliseconds
            # The solution is built on https://github.com/doctrine/dbal/issues/2873#issuecomment-701052412
            # but instead of using microseconds we use milliseconds
            datetime: Datana\Doctrine\Type\Doctrine\DBAL\Types\Type\DateTimeMillisecondsType
```

[build-status-master-php]: https://github.com/datana-gmbh/doctrine-type-testcases/workflows/PHP/badge.svg?branch=master
[coverage-status-master]: https://codecov.io/gh/datana-gmbh/doctrine-type-testcases/branch/master/graph/badge.svg

[actions]: https://github.com/datana-gmbh/doctrine-type-testcases/actions
[codecov]: https://codecov.io/gh/datana-gmbh/doctrine-type-testcases

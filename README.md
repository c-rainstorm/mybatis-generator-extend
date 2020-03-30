# Quick Start

- [Quick Start](#quick-start)
  - [clone or download this rep](#clone-or-download-this-rep)
  - [open in IDEA directly](#open-in-idea-directly)
  - [add `generatorConfig.properties`](#add-generatorconfigproperties)
  - [run `mybatis-generator` already configed](#run-mybatis-generator-already-configed)
  - [Advented](#advented)

## clone or download this rep

## open in IDEA directly

There is an runConfigurations `.idea/runConfigurations/mybatis_generator.xml` ready to use.

## add `generatorConfig.properties`

Add the `generatorConfig.properties` file to the `do-generate` module `test/resources` directory and save the following configuration

```properties
# datasource config
jdbc.driver=com.mysql.jdbc.Driver
jdbc.url=jdbc:mysql://xxxx:3306/boot?characterEncoding=utf-8
jdbc.username=xxxx
jdbc.password=xxxx

# the table need generate DO object and mapper
table.name=user

# mapper target package
mapper.package=me.rainstorm.mybatis.dao

# DO object target package
model.package=me.rainstorm.mybatis.domain
```

## run `mybatis-generator`

## Example

```properties
# the table need generate DO object and mapper
table.name=user

# mapper target package
mapper.package=me.rainstorm.mybatis.dao

# DO object target package
model.package=me.rainstorm.mybatis.domain
```

produce:

- `me.rainstorm.mybatis.dao.UserMapper` in `do-generate/src/main/java`
- `me.rainstorm.mybatis.domain.UserDO`  in `do-generate/src/main/java`
- `/mybatis/mapper/UserDOMapper.xml` in `do-generate/src/main/resources`

## At Last

detail generator config, please see [`generatorConfig.xml`](do-generate/src/test/resources/generatorConfig.xml)
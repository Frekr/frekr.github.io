###Symfony configuration

In order to use Propel configure few parameters in `app/config/config.yml` file.

If you are not using Composer, add this configuration:

~~~yaml
# in app/config/config.yml
propel:
    path:       "%kernel.root_dir%/../vendor/propel"
    phing_path: "%kernel.root_dir%/../vendor/phing"
~~~

###Basic Configuration

If you have just one database connection, use of this parameters is recommended:

~~~yaml
# app/config/config*.yml
# define the parameters in app/config/parameters.yml
propel:
    dbal:
        driver:               %database_driver%
        user:                 %database_user%
        password:             %database_password%
        dsn:                  %database_driver%:host=%database_host%;dbname=%database_name%;charset=UTF8
        options:              {}
        attributes:           {}
~~~

If you have more than one connection, or want to use a named connection, the configuration will look like:

~~~yaml
# app/config/config*.yml
propel:
    dbal:
        default_connection:         conn1
        connections:
            conn1:
                driver:             mysql
                user:               root
                password:           null
                dsn:                mysql:host=localhost;dbname=db1
            conn2:
                driver:             mysql
                user:               root
                password:           null
                dsn:                mysql:host=localhost;dbname=db2
~~~

####Configure Master/Slaves

~~~yaml
# app/config/config*.yml
propel:
    dbal:
        default_connection:         default
        connections:
            default:
                driver:             mysql
                user:               root
                password:           null
                dsn:                mysql:host=localhost;dbname=master
                slaves:
                    slave_1:
                        user:       root
                        password:   null
                        dsn:        mysql:host=localhost;dbname=slave_1
~~~

###Attributes, Options, Settings

~~~yaml
# app/config/config*.yml
propel:
    dbal:
        default_connection:         default
        connections:
            default:
                # ...
                options:
                    ATTR_PERSISTENT: false
                attributes:
                    ATTR_EMULATE_PREPARES: true
                settings:
                    charset:        { value: UTF8 }
                    queries:        { query: 'INSERT INTO BAR ('hey', 'there')' }
~~~

####Logging

~~~yaml
# in app/config/config.yml
propel:
    logging:    %kernel.debug%
~~~

###Propel Configuration

You can add a `app/config/propel.ini` file in your project to specify some configuration parameters.

By default the PropelBundle is configured with the default parameters:

~~~
# Enable full use of the DateTime class.
# Setting this to true means that getter methods for date/time/timestamp
# columns will return a DateTime object when the default format is empty.
propel.useDateTimeClass = true

# Specify a custom DateTime subclass that you wish to have Propel use
# for temporal values.
propel.dateTimeClass = DateTime

# These are the default formats that will be used when fetching values from
# temporal columns in Propel. You can always specify these when calling the
# methods directly, but for methods like getByName() it is nice to change
# the defaults.
# To have these methods return DateTime objects instead, you should set these
# to empty values
propel.defaultTimeStampFormat =
propel.defaultTimeFormat =
propel.defaultDateFormat =

# A better Pluralizer
propel.builder.pluralizer.class = builder.util.StandardEnglishPluralizer

###Build properties

You can define build properties by creating a `propel.ini` file in `app/config` like below, but you can also follow the Symfony2 convention by adding build properties in `app/config/config.yml`:

~~~yaml
# app/config/config.yml
propel:
    build_properties:
        xxxxx.xxxx.xxxxx:   XXXX
        xxxxx.xxxx.xxxxx:   XXXX
        // ...
~~~

####Behaviors¶

~~~yaml
# app/config/config.yml
propel:
    behaviors:
        behavior_name: My\Bundle\Behavior\BehaviorClassName
~~~     
# winston-transport-papertrail

[winston-transport](https://github.com/winstonjs/winston-transport) module for [papertrail](https://papertrailapp.com/).

# install

    # for npm
    npm install --save winston-transport-papertrail

    # for yarn
    yarn add winston-transport-papertrail


# es6 usage

    import winston from 'winston';
    import { WinstonTransportPapertrail } from 'winston-transport-papertrail';

    // define env configs received from papertrail log destination settings
    // @url https://papertrailapp.com/account/destinations
    const HOST = 'logs5.papertrailapp.com'; // replace this from the value you receive from above.
    const PORT = '12456'; // replace this from the value you receive from above.
    const LEVEL = 'debug'; // @url https://github.com/winstonjs/winston#logging-levels

    winston.add(winston.transports.WinstonTransportPapertrail, options);
    // or
    const logger = new winston.Logger({ transports: [new WinstonTransportPapertrail({
        papertrailConfig: {
          host: HOST,
          port: PORT,
          level: LEVEL,
        },
      })]
    });

# es5 usage

    var winston = require('winston');

    //
    // Requiring `winston-papertrail` will expose
    // `winston.transports.WinstonTransportPapertrail`
    //
    require('winston-transport-papertrail').WinstonTransportPapertrail;

    winston.add(winston.transports.WinstonTransportPapertrail, options);
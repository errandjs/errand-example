# errand-example
> example demonstrating how to use [errand](https://github.com/errandjs/errand) producer and worker

## Usage

```

npm install

pm2 start .\node_modules\errand-logger\lib\errand-logger.js

node ./node_modules/errand/lib/errand-producer.js --job .\errand-sample-job.json

```

Notes:

1. For dependencies refer to [errand](https://github.com/errandjs/errand)
2. Suggested usage requires [pm2](http://pm2.keymetrics.io/)
3. Example uses the [errand-logger](https://github.com/errandjs/errand-logger) component which will console.log `data.request.message`.

## Example Task List

```

{
	"tasks": [

		{
			"task": "errand-logger",
			"data": {
				"name": "errand-logger-task-1",
				"request": {
					"message": "hello world"
				}
			}
		},
		{
			"task": "errand-logger",
			"data": {
				"name": "errand-logger-task-2",
				"request": {
					"message": "foobar"
				}
			}
		}

	]
}

```


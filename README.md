![uptime-badge](https://socialify.git.ci/sooluh/uptime-badge/image?description=1&descriptionEditable=Simple%20JSON%20endpoint%20to%20display%20shields.io%20badge%20based%20on%20uptime%20status%20from%20betteruptime.com&font=Raleway&forks=1&issues=1&language=1&logo=https%3A%2F%2Fraw.githubusercontent.com%2Ftwitter%2Ftwemoji%2Fmaster%2Fassets%2Fsvg%2F26a1.svg&owner=1&pattern=Charlie%20Brown&pulls=1&stargazers=1&theme=Dark)

## Getting Started

1. Clone this repository

   ```bash
   git clone https://github.com/sooluh/uptime-badge.git
   cd uptime-badge
   ```

2. Install dependencies

   ```bash
   yarn install
   ```

3. Run the app!

   - Development mode

     ```bash
     yarn dev
     ```

   - Production mode

     1. Build first

        ```bash
        yarn build
        ```

     2. Start the app

        ```bash
        yarn start
        ```

### Environment Variable

| Key                  | Value                                                                                        |
| -------------------- | -------------------------------------------------------------------------------------------- |
| `BETTERUPTIME_TOKEN` | Get it from the Integration menu on your [Better Uptime](https://betteruptime.com) dashboard |

### One-click Deployment

The fastest way to use it privately on PaaS available

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fsooluh%2Fuptime-badge%2Ftree%2Fmain)
[![Deploy with Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https%3A%2F%2Fgithub.com%2Fsooluh%2Fuptime-badge)

## Basic Usage

Base URL : [`https://uptime-badge.vercel.app/:id`](https://uptime-badge.vercel.app/:id)

**Notes :**<br>

> `:id` is the monitor id in Better Uptime.

|   Query string | Default Value | Description                                                                             |
| -------------: | ------------- | --------------------------------------------------------------------------------------- |
|        `label` | `website`     | Text displayed on the left                                                              |
|  `label_color` | `#555`        | Background color for the left side                                                      |
|        `style` | `flat`        | Default template to use                                                                 |
| `down_message` | `down`        | The text on the right that is displayed if it is detected is down                       |
|   `down_color` | `#e05d44`     | Right side background color if detected down                                            |
|   `up_message` | `up`          | The text on the right that is displayed if it is detected is up                         |
|     `up_color` | `#4c1`        | Right side background color if detected up                                              |
|         `logo` | `none`        | One of the named logos supported by Shields or [simple-icons](https://simpleicons.org/) |
|   `logo_color` | `none`        | Color of the logo to be displayed                                                       |

### Example of Use

1. Compose the URL endpoint first

   <pre><a href="https://uptime-badge.vercel.app/675310?label=production&down_message=offline&up_message=online">http://uptime-badge.vercel.app/675310?<strong>label=production</strong>&<strong>down_message=offline</strong>&<strong>up_message=online</strong></a></pre>

2. Encode URL with [urlencoder.org](https://urlencoder.org) and paste into the query string `?url=` at the shields.io endpoint

   ```
   https%3A%2F%2Fuptime-badge.vercel.app%2F675310%3Flabel%3Dproduction%26down_message%3Doffline%26up_message%3Donline
   ```

   ```
   https://img.shields.io/endpoint?url=https%3A%2F%2Fuptime-badge.vercel.app%2F675310%3Flabel%3Dproduction%26down_message%3Doffline%26up_message%3Donline
   ```

3. Result

   ![](https://img.shields.io/endpoint?url=https%3A%2F%2Fuptime-badge.vercel.app%2F675310%3Flabel%3Dproduction%26down_message%3Doffline%26up_message%3Donline)

### License

Code licensed under [Apache 2.0 License](https://github.com/sooluh/uptime-badge/blob/main/LICENSE).

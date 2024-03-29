# Image Prediction App

## Getting Started

### Prerequisites

To install the software, you will need the following:

Node.js and npm:
You can install the latest version of npm globally by running the command `npm install npm@latest -g`.
You can install Node.js using nvm (Node Version Manager) by running `nvm install v20`.

### Installation

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Then run the json server in a separate terminal:

```bash
npx json-server public/assets/db.json -p 8000
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the Images tab.

## The Brief

The application has 2 tabs: Images & Predictions.

#### Images

This tab gives the user capability to upload into memory (no need to call an API here) and manage a list of images which will be used for further processing. The list of images should be displayed in a tabular format with the following columns:

- Filename of the Image
- Size of the image
- Time of Upload
- A button called "PREDICT".

On clicking the PREDICT button, a modal will open, wherein:

- The user is asked to fill out a ‘Title’ and ‘Description’ for the prediction should be displayed. The user can either submit the prediction or cancel the operation:
- On clicking submit the request to the JSON server is made, saving the response against the image.
  - On successful completion of the API request a single new entry would be added to the Predictions tab.

#### Predictions

This tab gives users the ability to view the predictions generated by this app. The list of predictions are displayed in a tabular format with the following columns:

- Title (as selected by the user when submitting the prediction)
- Description (as selected by the user when submitting the prediction)
- Timestamp of running the prediction
- Button called VIEW

On clicking the VIEW button, the following happens:

- The image on which the prediction was run is displayed.
- All the items in the prediction of this image are displayed.
- A transparent rectangle covering the coordinates in the prediction item is displayed
  over the image for all items predicted within an image, the image and prediction are
  responsive.
- The “label” and “score” should be displayed along with the prediction for the item.

## Authors

Ravneet Singh Anand - [RavneetAnand](https://github.com/RavneetAnand)

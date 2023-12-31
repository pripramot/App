

# Vertex AI Conversation 
## Overview

[Data Store Agent](https://cloud.google.com/generative-ai-app-builder/docs/agent-intro)
is a feature within
[Vertex AI Conversation](https://cloud.google.com/generative-ai-app-builder)
that is built on top of functionality in
[Dialogflow CX](https://cloud.google.com/dialogflow).

[Vertex AI Conversation Demo](static/vertex-ai-conversation.png)

ด้วย Data Store Agent คุณสามารถระบุโดเมนเว็บไซต์ ข้อมูลที่มีโครงสร้าง หรือ
ข้อมูลที่ไม่มีโครงสร้าง จากนั้น Data Store Agent จะวิเคราะห์เนื้อหาของคุณและสร้าง
ตัวแทนเสมือนที่ขับเคลื่อนโดยแหล่งเก็บข้อมูลและโมเดลภาษาขนาดใหญ่ ของคุณ
ลูกค้าและผู้ใช้ปลายทางสามารถสนทนากับตัวแทนและถามได้
คำถามเกี่ยวกับเนื้อหา
[Data Store Agent documentation](https://cloud.google.com/generative-ai-app-builder/docs/agent-usage)
และ codelab โปรดดูข้อมูลเพิ่มเติมที่
[Create a Generative Chat App with Vertex AI Conversation](https://codelabs.developers.google.com/codelabs/vertex-ai-conversation)


## ขั้นตอนในการสร้างเว็บแอป

1. Install [Node.js](https://nodejs.org/en) using your preferred method or
   package manager
1. From this directory, run `npm install`
1. Run `npm run build` to generate the static site in the `build` directory

## ขั้นตอนในการปรับใช้เว็บแอปกับ Firebase

1. Navigate to the [Firebase console](https://console.firebase.google.com/)
1. Provision Firebase on a new or existing GCP project
1. In Firebase console, go to Hosting and add a new site (e.g.,
   `your-firebase-app-name`)
1. Install the [firebase CLI](https://firebase.google.com/docs/cli)
1. Run `firebase init` in the app root and follow the prompts to select
   `Hosting`, use the `build` directory, and confirm `N` to the followup
   questions about rewrites, deploys, and the 404 and index pages.
1. Run
   `firebase target:apply hosting your-firebase-app-name your-firebase-app-name`
   where `your-firebase-app-name` is the name of the Firebase Hosting site that
   you created in an earlier step
1. To configure the default deploy target, add a line to your `firebase.json`
   with the name of your Firebase Hosting site, such as:

   ```json
   {
     "hosting": {
       "target": "your-firebase-app-name",  # <--- Add this line
       "public": "build",
       "ignore": [
         "firebase.json",
         "**/.*",
         "**/node_modules/**"
       ]
     }
   }
   ```

1. Run `firebase deploy`

## Access the app

In your browser, navigate to your deployed app using a URL similar to:

[https://vertex-ai-conversation.web.app/](https://vertex-ai-conversation.web.app/)

Congratulations, you've successfully deployed the Vertex AI Conversation Demo!

## Additional resources

คุณสามารถเรียนรู้เกี่ยวกับ AI เชิงสนทนาและ AI เชิงสร้างสรรค์ต่อไปได้
คำแนะนำและแหล่งข้อมูลเหล่านี้:

- [Overview of Vertex AI Conversation](https://cloud.google.com/generative-ai-app-builder/docs/agent-intro)
- [Create and use Data Store Agents](https://cloud.google.com/generative-ai-app-builder/docs/agent-usage)
- [Documentation for Dialogflow CX](https://cloud.google.com/dialogflow/cx/docs)
- [Documentation for Data Store Agents](https://cloud.google.com/dialogflow/cx/docs/concept/data-store-agent)
- [Generative AI in Google Cloud](https://cloud.google.com/ai/generative-ai)

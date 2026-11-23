## Definition
AWS Elastic Transcoder is a fully-managed video-transcoding service that converts videos from one format to another for Video-on-Demand (VOD) or streaming video. 

- AWS elastic transcoder cannot be used via AWS CFN
    - If you need to automate you need to use the AWS SDK or AWS CLI

- Create a pipeline
    - Create a job
        - Choose a preset (determines what to cover the file to)
        - Choose source and destination bucket


> AWS Elemental MediaConvert is the modern version of Elastic Transcoder. AWS Elastic Transcoder exists for legacy customers who have not migrated to MediaConvert 
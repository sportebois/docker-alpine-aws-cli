# Alpine AWS-CLI


## How to use it

Either inject some AWS credentials using env vars, or mouns your local credentials (or any other way for the boto, as [described in the docs](https://boto3.readthedocs.io/en/latest/guide/configuration.html#environment-variables) )

The default entrypoint is already the 'aws' command, so you can directly pull the image, retag it to something shorter, then use it at will:

        docker pull 809113430512.dkr.ecr.us-east-1.amazonaws.com/alpine-aws-cli:latest
        docker tag 809113430512.dkr.ecr.us-east-1.amazonaws.com/alpine-aws-cli:latest aws-cli:latest

        docker run -it --rm -v $HOME/.aws:/root/.aws:ro aws-cli ec2 describe-instances --region eu-central-1

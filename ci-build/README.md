
* Fork https://github.com/aws-samples/eks_gpu_and_trainuim_perceiver_io_training/ and populate the `GITHUB_USER`.
* Export the following variables

```bash
export AWS_ACCOUNT_ID=$(aws sts get-caller-identity --output text --query Account)
export AWS_REGION=us-west-2
export BASE_IMAGE_AMD_XLA_TAG=1.13.1-neuronx-py310-sdk2.14.1-ubuntu20.04
export BASE_IMAGE_AMD_CUD_TAG=2.0.1-cpu-py310-ubuntu20.04-ec2
export IMAGE_AMD_XLA_TAG=amd64-neuron
export IMAGE_AMD_CUD_TAG=amd64-cuda
export BASE_REPO=perceiver
export BASE_TAG=multiarch-ubuntu
export BASE_ARM_TAG=arm64
export BASE_AMD_TAG=amd64
export GITHUB_BRANCH=master
export GITHUB_USER=yahavb
export GITHUB_REPO=eks_gpu_and_trainuim_perceiver_io_training
```

```bash
cd ci-build
./deploy-pipeline.sh
```

const capture=new CaptureManager();

//拍照

const photo=await capture.safeCapture('image');

//拍视频
const video=await capture,safeCapture('video);


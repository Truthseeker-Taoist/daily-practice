//相片媒体采集管理器
import {AUYH_SCOPES} from './auth-config';

class CaptureManager{
//**
 *核心方法：安全采集媒体
 *@param{String} type - 'image' 或 'video'
 */
 async safeCapture(type'=image'){
  try{
//.权限预检
await
this.checkPermission(AUTH_SCOPES.CAMERA)

//.执行调度采集
const result=await this.execCapture(type);
return result;
} catch(error){
  console.error('采集失败:',error);
  wx,showToast({title:error.message||'操作取消',
  icon:'none'});
   throw.error;
}
 }

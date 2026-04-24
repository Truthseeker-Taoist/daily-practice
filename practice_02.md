//定位获取管理器
import {AUTH_SCOPES} from ‘./auth.config’

class LocationManager{
  async safeGatLocation(){
  try(){
  await this._checkPermission(AUTH.SCOPES);
  const result =await this.execgetLocation();
  return result;
  }catch(error){
   console.error("定位失败：";error);
   wx.showToast({title.error.message ||'获取定位失败'，icon,'none'});
   throw error;
  }
  }
}

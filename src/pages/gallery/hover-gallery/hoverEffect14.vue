<template>
    <div class="row">
              <div class="col-sm-12 ">
                <div class="card">
                  <div class="card-header ">
                    <h5>Hover Effect <span class="digits">14</span></h5>
                  </div>
                  <div class="card-body">
                    <div class="row my-gallery gallery" id="aniimated-thumbnials" itemscope="" data-pswp-uid="1">
                      <figure class="col-md-3 col-6 img-hover hover-14" 
                              v-for="(n,index) in gallery1"  :key="index" 
                              itemprop="associatedMedia" itemscope="">
                          
                            <div>
                              <img :src="getpath(n)" itemprop="thumbnail" alt="Image description" class="img-fluid">
                            </div>
                      </figure>
                    </div>
                  </div>
                </div>
              </div>
            </div> 
</template>
<script>
export default {
     data(){
        return{
            gallery1: [
          '08.jpg',
          '09.jpg',
          '010.jpg',
          '011.jpg'
        ],
        }
    },
     methods: {
       getpath(filename) {
        return require('@/assets/images/lightgallry/' + filename);
      }
    }
}
</script>
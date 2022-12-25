<template>





    <div class="container"><h2>Add Product</h2>
        
       
        


        <div class="mb-3">
        <label for="exampleFormControlInput1" class="form-label">Product Name</label>
        <input name="productName" 
        type="text" 
        class="form-control" 
        
        placeholder="Product Name"
        v-validate="'required'"
        v-model="item.productName"
        
        autofocus>
        <div v-show="errors.has('productName')" class="help-block alert alert-danger">{{errors.first('productName')}}</div>
        </div>

        <div class="mb-3">
        <label for="exampleFormControlInput1" class="form-label">Product Catagory</label>
        <input 
        name="productCatagory"
        type="text" 
        class="form-control" 
        
        placeholder="Product Catagory"
        v-validate="'required'"
        v-model="item.productCatagory">
        
        <div v-show="errors.has('productCatagory')" class="help-block alert alert-danger">{{errors.first('productCatagory')}}</div>
        </div>

        <div class="mb-3">
        <label for="exampleFormControlInput1" class="form-label">Quantity</label>
        <input 
        name="productQuantity"
        type="number" 
        class="form-control" 
        
        placeholder="Quantity"
        v-validate="'required|max_value:5'"
        v-model="item.productQuantity">
        <div v-show="errors.has('productQuantity')" class="help-block alert alert-danger">{{errors.first('productQuantity')}}</div>
        </div>



        <div class="mb-3">
        <label for="exampleFormControlTextarea1" class="form-label">Description</label>
        <textarea 
        name="productDescription"
        class="form-control" 
        
        rows="3"
        v-validate="'required'"
        v-model="item.productDescription"></textarea>
        <div v-show="errors.has('productDescription')" class="help-block alert alert-danger">{{errors.first('productDescription')}}</div>
        </div>

        <div class="mb-3">
        <label for="exampleFormControlInput1" class="form-label">Unit Price in LKR</label>
        <input 
        name="unitPrice"
        type="number" 
        class="form-control" 
        
        placeholder="unit price"
        v-validate="'required|max:10'"
        v-model="item.unitPrice">
        <div v-show="errors.has('unitPrice')" class="help-block alert alert-danger">{{errors.first('unitPrice')}}</div>
        </div>

        <div class="mb-3">
        <label for="formFile" class="form-label">Default file input example</label>
        <input class="form-control" type="file" id="formFile">
        </div>

        <div class="form-group">
        <div class="col-sm-offset-2 col-sm-10">
        <button 
        type="Submit" 
        class="btn btn-secondary"
        v-show="item.productName && item.productCatagory && item.productQuantity && item.productDescription && item.unitPrice"
        >Add to the List</button>
        </div></div>

    </div>
</template>
<script>

export default{
    data(){
        return{
            item:{
                productName:'',
                productCatagory:'',
                productQuantity:0,
                productDescription:'',
                unitPrice:0
            }
        }
    }
}






</script>
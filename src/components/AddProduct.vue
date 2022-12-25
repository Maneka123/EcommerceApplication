<template>





    <div class="container"><h2>Add Product</h2>
        
       
        


        <div class="mb-3">
        <label for="exampleFormControlInput1" class="form-label">Product Name</label>
        <input name="productName" 
        type="text" 
        class="form-control" 
        id="exampleFormControlInput1" 
        placeholder="Product Name"
        v-validate="'required'"
        
        autofocus>
        <div v-show="errors.has('productName')" class="help-block alert alert-danger">{{errors.first('productName')}}</div>
        </div>

        <div class="mb-3">
        <label for="exampleFormControlInput1" class="form-label">Product Catagory</label>
        <input 
        name="productCatagory"
        type="text" 
        class="form-control" 
        id="exampleFormControlInput1" 
        placeholder="Product Catagory"
        v-validate="'required'">
        
        <div v-show="errors.has('productCatagory')" class="help-block alert alert-danger">{{errors.first('productCatagory')}}</div>
        </div>

        <div class="mb-3">
        <label for="exampleFormControlInput1" class="form-label">Quantity</label>
        <input 
        name="productQuantity"
        type="number" 
        class="form-control" 
        id="exampleFormControlInput1" 
        placeholder="Quantity"
        v-validate="'required|max_value:5'">
        <div v-show="errors.has('productQuantity')" class="help-block alert alert-danger">{{errors.first('productQuantity')}}</div>
        </div>



        <div class="mb-3">
        <label for="exampleFormControlTextarea1" class="form-label">Description</label>
        <textarea 
        name="productDescription"
        class="form-control" 
        id="exampleFormControlTextarea1" 
        rows="3"
        v-validate="'required'"></textarea>
        <div v-show="errors.has('productDescription')" class="help-block alert alert-danger">{{errors.first('productDescription')}}</div>
        </div>

        <div class="mb-3">
        <label for="exampleFormControlInput1" class="form-label">Unit Price in LKR</label>
        <input 
        name="unitPrice"
        type="number" 
        class="form-control" 
        id="exampleFormControlInput1" 
        placeholder="unit price"
        v-validate="'required|max:10'">
        <div v-show="errors.has('unitPrice')" class="help-block alert alert-danger">{{errors.first('unitPrice')}}</div>
        </div>

        <div class="mb-3">
        <label for="formFile" class="form-label">Default file input example</label>
        <input class="form-control" type="file" id="formFile">
        </div>

        <div class="form-group">
        <div class="col-sm-offset-2 col-sm-10">
        <button type="Submit" class="btn btn-secondary">Add to the List</button>
        </div></div>

    </div>
</template>
<script></script>
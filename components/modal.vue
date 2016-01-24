

<script>
  export default {
    props: ['name', 'descript'],

    watch: {
      name () {
        jQuery(this.$els.modal).modal('show')
      }
    }
  }
</script>

<template>
    <div v-el:modal class="modal fade" tabindex="-1" role="dialog">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
            <h4 class="modal-title">{{ name }}</h4>
          </div>
          <div class="modal-body">
            {{ descript }}
          </div>
        </div><!-- /.modal-content -->
      </div><!-- /.modal-dialog -->
    </div><!-- /.modal -->
</template>
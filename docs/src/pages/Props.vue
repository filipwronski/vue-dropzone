<template>
  <div>
    <h1>Props</h1>
    <p>The following props are available for the Vue2-Dropzone component.</p>
    <simple-table :headers="['Prop Name', 'Type', 'Default', 'Description', 'Required']" :rows="props" />
    <edit-doc :link="'Props.vue'"></edit-doc>
  </div>
</template>

<script>
import SimpleTable from '../components/SimpleTable.vue';
import editDoc from '../components/DocEditLink.vue';

export default {
  data: function() {
    return {
      props: [
        ['id', 'String','dropzone', 'A string by which to identify the component, can be anything', 'True'],
        ['options', 'Object','{}', 'A dropzone [configuration object](http://www.dropzonejs.com/#configuration-options), accepts all valid dropzone configuration', 'True'],
        ['includeStyling', 'Boolean','True', 'Whether to include the dropzone and component styling.', 'False'],
        ['awss3', 'Object','{}', 'Object consisting of 3 values signingURL, headers, and params. You can use the headers and params keys to send additional headers or parameters with the signing request (e.g. CSRF tokens). See [Demo and config](#/aws-s3-upload)', 'False'],
        ['destroyDropzone', 'Boolean','True', 'Destroy the dropzone object when the component is destroyed.', 'False'],
        ['duplicateCheck','Boolean','False','Check if added file is duplicate, in already dropped files in dropzone','False'],
        ['useCustomSlot','Boolean','False','Use a custom slot for the default message area','False'],
      ]
    }
  },
  components: {
    'simple-table': SimpleTable,
    'edit-doc': editDoc
  }
}
</script>


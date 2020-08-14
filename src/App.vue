<template>
  <div id="app">
    <i-container class="main-container">
      <h2>Markdown</h2>
      <i-row>
        <i-column sm="6">
          <i-textarea
              v-model="text"
              rows="25"
              placeholder="Type something..">
          </i-textarea>
        </i-column>
        <i-column class="borderleft" sm="6">
          <div>
            <vue-markdown :source="text">
            </vue-markdown>
          </div>
        </i-column>
      </i-row>
    </i-container>
  </div>
</template>


<script>
import VueMarkdown from 'vue-markdown'

export default {
  name: 'App',
  components: {
    VueMarkdown
  },
  data() {
    return {
      text: '# h1 Heading :-)\n' +
          '## h2 Heading\n' +
          '### h3 Heading\n' +
          '\n' +
          '## Emphasis\n' +
          '\n' +
          '**This is bold text**\n' +
          '\n' +
          '__This is bold text__\n' +
          '\n' +
          '*This is italic text*\n' +
          '\n' +
          '_This is italic text_\n' +
          '\n' +
          '~~Strikethrough~~\n' +
          '\n' +
          '## Blockquotes\n' +
          '\n' +
          '> Blockquotes can also be nested...\n' +
          '>> ...by using additional greater-than signs right next to each other...\n' +
          '> > > ...or with spaces between arrows.\n' +
          '\n' +
          '## Lists\n' +
          '\n' +
          'Unordered\n' +
          '\n' +
          '+ Create a list by starting a line with `+`, `-`, or `*`\n' +
          '+ Sub-lists are made by indenting 2 spaces:\n' +
          '  - Marker character change forces new list start:\n' +
          '    * Ac tristique libero volutpat at\n' +
          '    + Facilisis in pretium nisl aliquet\n' +
          '    - Nulla volutpat aliquam velit\n' +
          '+ Very easy!\n' +
          '\n' +
          'Ordered\n' +
          '\n' +
          '1. Lorem ipsum dolor sit amet\n' +
          '2. Consectetur adipiscing elit\n' +
          '3. Integer molestie lorem at massa\n' +
          '\n' +
          '1. You can use sequential numbers...\n' +
          '1. ...or keep all the numbers as `1.`\n' +
          '\n' +
          'Start numbering with offset:\n' +
          '\n' +
          '57. foo\n' +
          '1. bar\n' +
          '\n' +
          '## Tables\n' +
          '\n' +
          '| Option | Description |\n' +
          '| ------ | ----------- |\n' +
          '| data   | path to data files to supply the data that will be passed into templates. |\n' +
          '| engine | engine to be used for processing templates. Handlebars is the default. |\n' +
          '| ext    | extension to be used for dest files. |\n' +
          '\n' +
          'Right aligned columns\n' +
          '\n' +
          '| Option | Description |\n' +
          '| ------:| -----------:|\n' +
          '| data   | path to data files to supply the data that will be passed into templates. |\n' +
          '| engine | engine to be used for processing templates. Handlebars is the default. |\n' +
          '| ext    | extension to be used for dest files. |\n' +
          '\n' +
          '## Links\n' +
          '\n' +
          '[vue-markdown](https://github.com/miaolz123/vue-markdown)\n' +
          '\n' +
          '### Emojies\n' +
          '\n' +
          '> Classic markup: :wink: :cry: :laughing: :yum:\n' +
          '>\n' +
          '> Shortcuts (emoticons): :-) :-( 8-) ;)\n' +
          '\n' +
          '### Subscript / Superscript\n' +
          '\n' +
          '- 19^th^\n' +
          '- H~2~O\n' +
          '\n' +
          '### \\<ins>\n' +
          '\n' +
          '++Inserted text++\n' +
          '\n' +
          '### \\<mark>\n' +
          '\n' +
          '==Marked text==\n' +
          '\n' +
          '### Footnotes\n' +
          '\n' +
          'Footnote 1 link[^first].\n' +
          '\n' +
          'Footnote 2 link[^second].\n' +
          '\n' +
          'Inline footnote^[Text of inline footnote] definition.\n' +
          '\n' +
          'Duplicated footnote reference[^second].\n' +
          '\n' +
          '[^first]: Footnote **can have markup**\n' +
          '\n' +
          '    and multiple paragraphs.\n' +
          '\n' +
          '[^second]: Footnote text.\n' +
          '\n' +
          '### Abbreviations\n' +
          '\n' +
          'This is HTML abbreviation example.\n' +
          '\n' +
          'It converts "HTML", but keep intact partial entries like "xxxHTMLyyy" and so on.\n' +
          '\n' +
          '*[HTML]: Hyper Text Markup Language'
    }
  }
}
</script>

<style scoped>

h2 {
  text-align: center;
  margin: 20px auto;
}

.borderleft{
  border-left: 1px solid;
}

</style>

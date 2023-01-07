# Principais comandos Rspec

- `Bloco principal,´

```ruby
require 'rails_helper'

describe 'descrição do teste' do
    it 'descrição da tarefa' do
        #arrange
        #act
        #assert
    end
end
```
# Principais comandos

- `visit('/'), acessa uma rota`
- `expect(page).to have_content('conteúdo procurado'), verifica se o 'conteúdo procurado' existe`
- `expect(page).not_to have_content('conteúdo procurado'), verifica se o 'conteúdo procurado' não existe`

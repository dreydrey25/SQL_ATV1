-- Criar coluna 'favorites' na tabela 'alunos'
ALTER TABLE alunos
ADD COLUMN favorites varchar(3) DEFAULT 'Não';

-- Mudar o valor da coluna 'favorites' para 'Sim' nos amigos favoritos
UPDATE alunos
SET favorites = 'Sim'
WHERE id IN (3, 8, 9, 16, 22, 25, 26, 29, 30, 34);

-- Selecionar todos os amigos favoritos
SELECT * FROM alunos WHERE favorites = 'Sim';

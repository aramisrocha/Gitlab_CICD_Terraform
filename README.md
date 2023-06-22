# CICD_Gitlab_Terraform


# Introdução
<p> Esta configuração tem a funcao de demostrar como seria implementar um CICD no Gitlab de forma que toda a alteração feita no ambiente em Cloud fosse possivel somente com uma aprovação de Merge request no GITLAB </p>

<p> Primeiramente é adicionado as credencias da conta da CLOUD no caso AWS no Gitlab, em seguida no projeto do Gitlab é feito o bloqueio do commit na main e criado as branchs apply,destroy e dev, assim toda a esteira é configurada na arquivo .gitlab-ci.yml, sendo possivel fazer um terraform plan sem exigir merge request, para fazer um apply ou destroy é necessario fazer o commit do codigo nas respectivas branchs e fazer o merge request, o tfstate do terraform sera armazenado no S3 da AWS centralizando todas as alterações, so sera feita a implementação do codigo ao aprovar o merge request para a main.
</p>

# knockout_stage_2022_FIFA_world_cup
## Simulation of FIFA 2022 World Cup Knockout Stage using Machine Learning (with updates)

Simulação da fase eliminatória da Copa do Mundo FIFA 2022 usando aprendizado de máquina (com atualizações)

Baseado nos repositórios:

[1] Predição baseada em modelo de ML: - Simulation of FIFA 2022 World Cup using Machine Learning
https://medium.com/@sslp23/predicting-fifa-2022-world-cup-with-machine-learning-640f1d2d7e98
    https://github.com/sslp23/world_cup_sim

[2] Predição baseada em Distribuição de Poisson: https://github.com/ifrankandrade/fifa-world-cup-2022-prediction


A ideia é usar a base apresentada em [1] e expandi-la com outros modelos de ML e depois modelos de deep learning. Utilizar [2] como elemento de comparação com um modelo probabilístico. 

Não fiz alterações no core do código de [1]. Apenas para captura dos dados das partidas e quem efetivamente passou de fase.


## Instalar pacotes:
pip install bs4
pip install networkx
pip install ipykernel jupyter

pip install scikit-learn==0.24.1
pip install markupsafe==2.0

pip install pydot
pip install pydotplus
pip install graphviz

Ubuntu 20.04:
    sudo apt-get install graphviz


## OBSERVAÇÕES
### Problemas com o Jupyter Notebook? 

- Failed to start Jupyter in the environment 'Python 3.8.10 64-bit'.  ImportError: cannot import name 'app' from 'notebook' (/home/usuario/.local/lib/python3.8/site-packages/notebook/__init__.py)  View Jupyter [log](command:jupyter.viewOutput) for further details.
    - tente executar fora do VScode diretamente no terminal: python -m jupyter notebook
    - caso dê o seguinte erro: 
        - ImportError: cannot import name 'soft_unicode' from 'markupsafe' (/home/usuario/.local/lib/python3.8/site-packages/markupsafe/__init__.py)
        - The "ImportError: cannot import name 'soft_unicode' from 'markupsafe'" occurs because the soft_unicode method has been deprecated in markupsafe version 2.1. 
        - To solve the error, run the pip install markupsafe==2.0 command to install the last version of markupsafe that supports soft_unicode.(6 de nov. de 2022)

### Unpickle:
- UserWarning: Trying to unpickle estimator GradientBoostingClassifier from version 0.24.1 when using version 1.1.3. This might lead to breaking code or invalid results. Use at your own risk. For more info please refer to:
https://scikit-learn.org/stable/model_persistence.html#security-maintainability-limitations
- pip install scikit-learn==0.24.1
    - Resultado:
        ```
        Uninstalling scikit-learn-1.1.3:
            Successfully uninstalled scikit-learn-1.1.3
        Successfully installed scikit-learn-0.24.1
        ```

## Execução:
- Executar wc simulation updates.ipynb, que simula todas as fases da Copa do Mundo FIFA 2022.

    - A primeira fase é uma repetição dos resultados previstos em [1]. O que fiz foi atualizar a lista dos classificados.

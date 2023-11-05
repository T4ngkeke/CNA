function c_cor=HARD_DECODER_GROUPE1(c,H,MAX_ITER)
% c matrice de taille (N,1)
% H matrice de connexion taille (M,N), M nb de cNodes, N vNodes
[M,N]=size(H);
signalReceived=c;
for iteration=1:MAX_ITER
    % vérifier si la matrice entrée ait une erreur
    s=H*signalReceived;
    if s==zeros(M,1)
        c_cor=signalReceived;
        return
    end
    % calcul f
    f=zeros(1,N);
    for i=1:N
        f(1,i)=transpose(s)*H(:,1);
    end
    for i=1:N
        if f(1,i)>=2
            %inverse le bit correspondant
            if signalReceived(i,1)==1
                signalReceived(i,1)=0;
            else 
                signalReceived(i,1)=1;
            end
        end
    end

end
c_cor=signalReceived;
return
end

